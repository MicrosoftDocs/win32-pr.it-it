---
title: Preparazione dell'applicazione per le applicazioni a 64 bit Windows
description: Sono disponibili diverse funzionalità che semplificano lo sviluppo di applicazioni che verranno eseguite in applicazioni a 32 e a 64 bit Windows. La maggior parte di questi, ad esempio i nuovi tipi di dati, è descritta in Getting Ready for 64-bit Windows.
ms.assetid: 6559b0ab-17cf-4bec-bf2d-3a0da0a344d3
keywords:
- Toolkit a 64 bit a 64 bit Windows programmazione
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3b6c8d31b685e6f545aca4bdaac341fe25a3c96f458048808536899a8416120a
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120071621"
---
# <a name="preparing-your-application-for-64-bit-windows"></a>Preparazione dell'applicazione per le applicazioni a 64 bit Windows

Sono disponibili diverse funzionalità che semplificano lo sviluppo di applicazioni che verranno eseguite in applicazioni a 32 e a 64 bit Windows. La maggior parte di questi, ad esempio i nuovi tipi di dati, è descritta in [Getting Ready for 64-bit Windows](getting-ready-for-64-bit-windows.md).

Il toolkit a 64 bit fornito con Windows SDK include un compilatore MIDL a 64 bit, Midl.exe, per la generazione di stub nativi a 64 bit, nonché stub a 32 bit. Usare **l'opzione /env win64** per generare solo stub a 64 bit. L'impostazione predefinita è la generazione di stub doppi eseguiti su entrambe le piattaforme.

Si noti che MIDL a 64 bit supporta solo le modalità di ottimizzazione [**/Oicf**](/windows/desktop/Midl/-oi) e [**/Os.**](/windows/desktop/Midl/-os)

 

 