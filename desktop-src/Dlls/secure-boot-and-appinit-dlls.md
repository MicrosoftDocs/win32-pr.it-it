---
description: A partire da Windows 8, l'infrastruttura delle DLL AppInit è \_ disabilitata quando è abilitato l'avvio protetto.
ms.assetid: 3ADE71C7-7113-4D26-8D6D-5609CAF13397
title: DLL AppInit e avvio protetto
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 67db758eebbccd1916b5c2611c20598c3f4d25cc80cd2910be22a65b4222bbae
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119256021"
---
# <a name="appinit-dlls-and-secure-boot"></a>DLL AppInit e avvio protetto

A partire da Windows 8, l'infrastruttura delle DLL AppInit è \_ disabilitata quando è abilitato l'avvio protetto.

## <a name="about-appinit_dlls"></a>Informazioni sulle DLL AppInit \_

L'infrastruttura delle DLL AppInit offre un modo semplice per associare le API di sistema consentendo il caricamento di DLL personalizzate nello spazio degli indirizzi di ogni \_ applicazione interattiva. Le applicazioni e il software dannoso usano entrambe le DLL AppInit per lo stesso motivo di base, ovvero per associare le API. Dopo il caricamento, la DLL personalizzata può eseguire l'hook di un'API di sistema nota e implementare funzionalità alternative. Solo un piccolo set di moderne applicazioni legittime usa questo meccanismo per caricare le DLL, mentre un ampio set di malware usa questo meccanismo per compromettere i sistemi. Anche le DLL AppInit legittime possono causare involontariamente deadlock di sistema e problemi di prestazioni, pertanto l'utilizzo delle DLL AppInit non \_ \_ è consigliato.

## <a name="appinit_dlls-and-secure-boot"></a>DLL AppInit \_ e avvio protetto

Windows 8 adottato UEFI e l'avvio protetto per migliorare l'integrità complessiva del sistema e fornire una protezione avanzata da minacce sofisticate. Quando è abilitato l'avvio protetto, il meccanismo delle DLL AppInit viene disabilitato come parte di un approccio senza compromissione per proteggere i clienti \_ da malware e minacce.

Si noti che l'avvio protetto è un protocollo UEFI e non Windows 8 funzionalità. Altre informazioni su UEFI e sulla specifica del protocollo di avvio protetto sono disponibili all'indirizzo [https://www.uefi.org](https://www.uefi.org/) .

## <a name="appinit_dlls-certification-requirement-for-windows-8-desktop-apps"></a>Requisito di certificazione delle DLL AppInit \_ per le Windows 8 desktop

Uno dei requisiti di certificazione per Windows 8 desktop è che l'app non deve caricare DLL arbitrarie per intercettare le chiamate API Win32 usando il meccanismo delle DLL \_ AppInit. Per informazioni più dettagliate sui requisiti di certificazione, vedere la sezione 1.1 requisiti di certificazione per le Windows 8 [desktop.](../win_cert/certification-requirements-for-windows-desktop-apps.md)

## <a name="summary"></a>Riepilogo

-   Il meccanismo delle DLL AppInit non è un approccio consigliato per le applicazioni legittime perché può causare deadlock del sistema \_ e problemi di prestazioni.
-   Il meccanismo delle DLL AppInit \_ è disabilitato per impostazione predefinita quando è abilitato l'avvio protetto.
-   L'uso di DLL AppInit in un Windows 8 app desktop è un Windows di \_ certificazione dell'app desktop.

Vedere il white paper seguente per informazioni sulle DLL AppInit in Windows 7 e \_ Windows Server 2008 R2: [DLL AppInit in Windows 7 e Windows Server 2008 R2.](/previous-versions/windows/hardware/download/dn550976(v=vs.85))

 

 
