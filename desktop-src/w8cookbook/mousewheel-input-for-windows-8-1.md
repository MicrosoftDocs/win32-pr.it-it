---
title: Input MouseWheel per Windows 8.1
description: Input MouseWheel per Windows 8.1
ms.assetid: A178E86C-16A6-4DF5-9880-CF83F62AAF04
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cd9480280bf5526c8cd63c0703705c7ef742bff4
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "103855810"
---
# <a name="mousewheel-input-for-windows-81"></a>Input MouseWheel per Windows 8.1

## <a name="platform"></a>Piattaforma

<dl> Client-Windows 8.1  
Server-Windows Server 2012 R2  
</dl>

## <a name="description"></a>Descrizione

In Windows 8.1 gli eventi MouseWheel non vengono più recapitati in base allo stato attivo della tastiera come nelle versioni precedenti di Windows. In Windows 8.1, se il mouse è posizionato su un'app dello Store, MouseWheel verrà recapitato all'app; per motivi di compatibilità, tuttavia, se il mouse è posizionato su un'applicazione desktop, MouseWheel continuerà a essere recapitato in base allo stato attivo della tastiera.

## <a name="manifestations"></a>Manifestazioni

Quando il mouse passa sopra le app dello Store, MouseWheel scorre tutti i contenuti applicabili senza che l'utente debba fare clic sull'app dello Store. Questo vale anche per la schermata Start. Questa operazione rende lo scorrimento di MouseWheel un'interazione più semplice in Windows 8.1 rispetto a Windows 8.

## <a name="mitigation"></a>Strategia di riduzione del rischio

Per la maggior parte, questa modifica non dovrebbe avere alcun effetto sulle app esistenti. Se un'app dello Store ha ascoltato gli eventi MouseWheel solo dopo aver registrato un evento click del mouse, è probabile che l'app non risponda a MouseWheel fino a quando l'utente non l'ha fatto clic attivamente. Di conseguenza, l'aspetto più probabile è semplicemente che un'app continui a funzionare esattamente come in Windows 8. Per le app desktop, con lo stato attivo della tastiera non viene più assegnata un'app a Monopoli sull'input di MouseWheel, ma questo non è in alcun modo in grado di interrompere tali app. Quindi, non è necessaria alcuna mitigazione a breve termine.

## <a name="solution"></a>Soluzione

Gli sviluppatori di app dello Store dovrebbero ricevere eventi MouseWheel senza un evento di clic del mouse precursore. Non dovrebbero, ad esempio, restare in ascolto di eventi MouseWheel solo dopo la registrazione di un clic del mouse. Analogamente, le applicazioni desktop non devono tentare di acquisire gli eventi MouseWheel (ad esempio, impostando un hook di basso livello) quando hanno lo stato attivo della tastiera.

## <a name="tests"></a>Test

Gli sviluppatori di App Store devono eseguire test su Windows 8.1 per verificare che tutte le funzionalità di scorrimento funzionino ogni volta che si passa il mouse sull'app. Gli sviluppatori di app desktop devono eseguire test su Windows 8.1 per verificare che non stiano acquisendo gli eventi MouseWheel (in base alle linee guida indicate in precedenza).

 

 




