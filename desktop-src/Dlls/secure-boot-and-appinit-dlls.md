---
description: A partire da Windows 8, l' \_ infrastruttura delle DLL AppInit è disabilitata quando è abilitato l'avvio protetto.
ms.assetid: 3ADE71C7-7113-4D26-8D6D-5609CAF13397
title: AppInit dll e avvio protetto
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2915dda53959f2a403a62112385fe80e735cbfd4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106317817"
---
# <a name="appinit-dlls-and-secure-boot"></a>AppInit dll e avvio protetto

A partire da Windows 8, l' \_ infrastruttura delle DLL AppInit è disabilitata quando è abilitato l'avvio protetto.

## <a name="about-appinit_dlls"></a>Informazioni sulle \_ DLL AppInit

L' \_ infrastruttura dll di AppInit fornisce un modo semplice per associare le API di sistema consentendo il caricamento di DLL personalizzate nello spazio degli indirizzi di ogni applicazione interattiva. Le applicazioni e il software dannoso usano entrambe le DLL AppInit per lo stesso motivo di base, ovvero l'hook delle API; una volta caricata la DLL personalizzata, può associare un'API di sistema nota e implementare funzionalità alternative. Un piccolo set di applicazioni legittime moderne utilizza questo meccanismo per caricare le dll, mentre un ampio set di malware utilizza questo meccanismo per compromettere i sistemi. Anche le DLL AppInit legittime \_ possono causare involontariamente deadlock di sistema e problemi di prestazioni, pertanto l'uso di \_ DLL AppInit non è consigliato.

## <a name="appinit_dlls-and-secure-boot"></a>AppInit \_ dll e avvio protetto

Windows 8 ha adottato UEFI e l'avvio protetto per migliorare l'integrità complessiva del sistema e garantire una protezione avanzata da minacce sofisticate. Quando è abilitato l'avvio protetto, il \_ meccanismo DLL AppInit è disabilitato come parte di un approccio senza compromessi per proteggere i clienti da malware e minacce.

Si noti che l'avvio protetto è un protocollo UEFI e non una funzionalità di Windows 8. Altre informazioni su UEFI e sulla specifica del protocollo di avvio protetto sono disponibili in [https://www.uefi.org](https://www.uefi.org/) .

## <a name="appinit_dlls-certification-requirement-for-windows-8-desktop-apps"></a>\_Requisiti di certificazione delle DLL AppInit per le app desktop di Windows 8

Uno dei requisiti di certificazione per le applicazioni desktop di Windows 8 è che l'app non deve caricare dll arbitrarie per intercettare le chiamate all'API Win32 usando il \_ meccanismo DLL AppInit. Per informazioni più dettagliate sui requisiti di certificazione, vedere la sezione 1,1 relativa ai [requisiti di certificazione per le app desktop di Windows 8](../win_cert/certification-requirements-for-windows-desktop-apps.md).

## <a name="summary"></a>Riepilogo

-   Il \_ meccanismo DLL AppInit non è un approccio consigliato per le applicazioni legittime, in quanto può causare problemi di prestazioni e deadlock del sistema.
-   Il \_ meccanismo DLL AppInit è disabilitato per impostazione predefinita quando è abilitato l'avvio protetto.
-   L'uso \_ di DLL AppInit in un'app desktop di Windows 8 è un errore di certificazione di un'applicazione desktop Windows.

Vedere il white paper seguente per informazioni sulle DLL di AppInit in \_ Windows 7 e Windows server 2008 R2: [DLL AppInit in Windows 7 e windows Server 2008 R2](/previous-versions/windows/hardware/download/dn550976(v=vs.85)).

 

 
