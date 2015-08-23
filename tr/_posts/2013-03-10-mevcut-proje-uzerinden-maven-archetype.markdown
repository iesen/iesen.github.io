---
layout: post
title:  "Mevcut Proje Üzerinden Maven Archetype Oluşturmak"
date:   2015-03-10 11:33:55
---

Eğer maven kullanıyorsanız, projelerin temel yapısını ve build döngüsünü tanımlamada kullanılan zengin konfigüre edilebilen, convention over configuration (default davranışı değiştirmek için konfigurasyon tanımlama) prensibini kullanan bir araç olduğunu biliyorsunuzdur diyerek yazıma başlıyorum.

Çoğu zaman birbirine benzeyen projeler için dizin yapısında, kullanılan frameworklerin konfigurasyon dosyalarında, test ve diğer build safhalarında aynı ayarları kullanırız. Her seferinde sıfırdan aynı proje yapısını oluşturma zahmetine girmektense, Maven da archetype denilen template yapılar kullanılabilir. Archetypelar da normal artifactlar gibi jar halinde paketlenip, repositorylere atılır. Sonradan bu archetypelar proje oluşturma aşamasında kullanılır. Central repository de (repo1.maven.org/maven2) bir çok farklı amaç için archetype bulunmaktadır. Aşağıda bu archetytpeları nasıl kullanacağımızdan tekrar bahsedeceğim.

Lafı fazla uzatmadan üzerinde çalıştığımız proje ile nasıl archetype üretip, tekrar kullanmak üzere repository ye deploy edeceğimize gelelim.

Öncelikle archetype üreteceğimiz projeyi açıp, tercih ettiğimiz ortak kullanılacak minimum bir halde bırakıp, gereksiz gördüğümüz dosyaları silerek işe başlıyoruz.

Maven archetype plugini ile plugin dosyalarını oluşturuyoruz: