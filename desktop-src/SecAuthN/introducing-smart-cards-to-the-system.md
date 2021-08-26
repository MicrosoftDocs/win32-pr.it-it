---
description: Prima che smart card sottosistema possa trovare un smart card, è necessario smart card il sottosistema.
ms.assetid: 5b331d7d-9440-4e0d-a73b-48a2a556c31c
title: Introduzione delle smart card al sistema
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 07cd65135e1580792135a1042729f2002f4437697fa0548a4f6cd776650485b5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120015711"
---
# <a name="introducing-smart-cards-to-the-system"></a>Introduzione delle smart card al sistema

Prima che [*smart card sottosistema possa*](../secgloss/s-gly.md) trovare un [*smart card*](../secgloss/s-gly.md), smart card deve essere introdotto nel sistema. Questa operazione viene in genere eseguita con smart card strumento di configurazione fornito dal produttore della scheda. Lo strumento può essere disponibile come programma su un disco floppy (con smart card), un controllo ActiveX disponibile in un sito Web e così via.

Lo strumento di installazione deve fornire le informazioni seguenti sulla scheda:

-   La [*relativa stringa ATR*](../secgloss/a-gly.md)e una maschera facoltativa da usare come supporto per l'identificazione della scheda.
-   Elenco di smart card supportate dalla scheda.
-   Nome visualizzato per la scheda da usare per identificare la scheda per l'utente. Nella maggior parte dei casi, l'utente lo fornirà al programma di installazione.
-   Provider [*di servizi primario*](../secgloss/p-gly.md) associato alla scheda (facoltativo), da usare quando si accede alla scheda tramite interfacce COM.

Per semplificare gli strumenti di installazione e garantire l'integrità del [*database smart card*](../secgloss/s-gly.md), il sottosistema smart card fornisce le due funzioni seguenti. [**SCardIntroduceCardType**](/windows/desktop/api/Winscard/nf-winscard-scardintroducecardtypea) introduce un smart card nel database e [**SCardForgetCardType**](/windows/desktop/api/Winscard/nf-winscard-scardforgetcardtypea) lo rimuove dal database.

 

 
