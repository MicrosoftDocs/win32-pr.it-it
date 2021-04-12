---
title: Preparazione dell'applicazione per Windows a 64 bit
description: Sono disponibili diverse funzionalità che semplificano lo sviluppo di applicazioni che verranno eseguite su Windows a 32 e 64 bit. La maggior parte di questi, ad esempio i nuovi tipi di dati, è descritta in preparazione per Windows a 64 bit.
ms.assetid: 6559b0ab-17cf-4bec-bf2d-3a0da0a344d3
keywords:
- Programmazione Windows a 64 bit Toolkit a 64 bit
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 76f3b40d2fb22b84abdd4322f476981dc54c7ad3
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "104224004"
---
# <a name="preparing-your-application-for-64-bit-windows"></a>Preparazione dell'applicazione per Windows a 64 bit

Sono disponibili diverse funzionalità che semplificano lo sviluppo di applicazioni che verranno eseguite su Windows a 32 e 64 bit. La maggior parte di questi, ad esempio i nuovi tipi di dati, è descritta in [preparazione per Windows a 64 bit](getting-ready-for-64-bit-windows.md).

Il Toolkit a 64 bit fornito con la Windows SDK include un compilatore MIDL a 64 bit, Midl.exe, per la generazione di stub a 64 bit nativi, oltre a Stub a 32 bit. Usare l'opzione **/ENV Win64** per generare solo stub a 64 bit. Per impostazione predefinita, vengono generati doppi Stub eseguiti su entrambe le piattaforme.

Si noti che MIDL a 64 bit supporta solo le modalità di ottimizzazione [**/Oicf**](/windows/desktop/Midl/-oi) e [**/OS**](/windows/desktop/Midl/-os) .

 

 