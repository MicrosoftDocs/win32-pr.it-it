---
description: Prima che il sottosistema smart card possa trovare una smart card, la smart card deve essere introdotta nel sistema.
ms.assetid: 5b331d7d-9440-4e0d-a73b-48a2a556c31c
title: Introduzione di smart card al sistema
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6b9134dd9efce17b60f3495bf7bfc36b03c34ed3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104233270"
---
# <a name="introducing-smart-cards-to-the-system"></a>Introduzione di smart card al sistema

Prima che il [*sottosistema Smart Card*](../secgloss/s-gly.md) possa trovare una [*Smart Card*](../secgloss/s-gly.md), la smart card deve essere introdotta nel sistema. Questa operazione viene in genere eseguita con uno strumento di configurazione della smart card fornito dal produttore della scheda. Lo strumento può essere un programma su un disco floppy (con la smart card), un controllo ActiveX disponibile in un sito Web e così via.

Lo strumento di installazione di deve fornire le seguenti informazioni sulla scheda:

-   La relativa [*stringa ATR*](../secgloss/a-gly.md)e una maschera facoltativa da usare come supporto per l'identificazione della scheda.
-   Elenco di interfacce di smart card supportate dalla scheda.
-   Nome visualizzato per la scheda da utilizzare per l'identificazione della scheda per l'utente. Nella maggior parte dei casi, l'utente lo fornirà allo strumento di configurazione di.
-   [*Provider di servizi primario*](../secgloss/p-gly.md) associato alla scheda (facoltativo), da utilizzare per l'accesso alla scheda tramite interfacce com.

Per semplificare gli strumenti di configurazione e per garantire l'integrità del [*database delle smart card*](../secgloss/s-gly.md), il sottosistema smart card fornisce le due funzioni seguenti. [**SCardIntroduceCardType**](/windows/desktop/api/Winscard/nf-winscard-scardintroducecardtypea) introduce una smart card nel database e [**SCardForgetCardType**](/windows/desktop/api/Winscard/nf-winscard-scardforgetcardtypea) la rimuove dal database.

 

 
