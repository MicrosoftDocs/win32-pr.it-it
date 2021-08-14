---
title: Input della rotellina del mouse per Windows 8.1
description: Input della rotellina del mouse per Windows 8.1
ms.assetid: A178E86C-16A6-4DF5-9880-CF83F62AAF04
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d2285d2a0456376b01289ac7a4c2607117441384ebd13b0aaf0a162eac50fdfb
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118211384"
---
# <a name="mousewheel-input-for-windows-81"></a>Input della rotellina del mouse per Windows 8.1

## <a name="platform"></a>Piattaforma

<dl> Client - Windows 8.1  
Server - Windows Server 2012 R2  
</dl>

## <a name="description"></a>Descrizione

In Windows 8.1, gli eventi relativi alla rotellina del mouse non vengono più recapitati in base all'attivazione della tastiera, come nelle versioni precedenti di Windows. In Windows 8.1, se il puntatore del mouse viene posizionato su un'app dello Store, la rotellina del mouse verrà recapitata all'app; Per motivi di compatibilità, tuttavia, se il puntatore del mouse viene posizionato su un'app desktop, la rotellina del mouse continuerà a essere recapitata in base allo stato attivo della tastiera.

## <a name="manifestations"></a>Manifestazioni

Quando si passa il mouse sulle app dello Store, la rotellina del mouse scorrerà qualsiasi contenuto applicabile senza che l'utente sia necessario fare clic sull'app dello Store. Questo vale anche per la schermata start. In questo modo lo scorrimento tramite rotellina del mouse è un'interazione più Windows 8.1 che in Windows 8.

## <a name="mitigation"></a>Strategia di riduzione del rischio

Nella maggior parte dei casi questa modifica non dovrebbe avere alcun impatto sulle app esistenti. Se un'app dello Store è in ascolto degli eventi della rotellina del mouse solo dopo aver registrato un evento clic del mouse, è probabile che l'app risponda alla rotellina del mouse solo dopo che l'utente ha fatto clic attivamente su di essa. Di conseguenza, lo svantaggio più probabile in questo caso è semplicemente che un'app continua a funzionare esattamente come in Windows 8. Per le app desktop, la presenza dello stato attivo della tastiera non offre più all'app un'attenzione particolare sull'input della rotellina del mouse, ma ciò non interrompe in alcun modo tali app. Non sono quindi necessarie mitigazioni a breve termine.

## <a name="solution"></a>Soluzione

Gli sviluppatori di app dello Store devono aspettarsi di ricevere eventi mousewheel senza un evento click del mouse. Non devono, ad esempio, restare in ascolto degli eventi relativi alla rotellina del mouse solo dopo la registrazione di un clic del mouse. Analogamente, le applicazioni desktop non devono tentare di acquisire gli eventi della rotellina del mouse (ad esempio, impostando un hook di basso livello) quando hanno lo stato attivo della tastiera.

## <a name="tests"></a>Test

Gli sviluppatori di app dello Store devono eseguire test Windows 8.1 per verificare che tutte le funzionalità di scorrimento funzionino ogni volta che il puntatore del mouse passa sull'app. Gli sviluppatori di app desktop devono testare Windows 8.1 per verificare che non acquisiscano gli eventi della rotellina del mouse (in base alle indicazioni precedenti).

 

 




