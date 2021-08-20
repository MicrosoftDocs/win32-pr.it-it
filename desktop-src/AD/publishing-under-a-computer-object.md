---
title: Pubblicazione in un oggetto computer
description: In genere, i servizi basati su host creano i criteri di sicurezza nell'oggetto computer per il computer host. I servizi basati su host sono servizi strettamente collegati a un singolo computer host.
ms.assetid: ecd7d8bc-4714-408a-856c-7cab8360bf81
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: aac659ab2bf482ee6d6c57dd1481e487d6e2af95dfd85a092f48f4928499b102
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119025359"
---
# <a name="publishing-under-a-computer-object"></a>Pubblicazione in un oggetto computer

In genere, i servizi basati su host creano i criteri di sicurezza nell'oggetto computer per il computer host. I servizi basati su host sono servizi strettamente collegati a un singolo computer host.

**Per creare i criteri di sicurezza in un oggetto computer**

1.  Chiamare la [**funzione GetComputerObjectName**](/windows/desktop/api/secext/nf-secext-getcomputerobjectnamea) per ottenere il nome distinto (DN) nella directory dell'oggetto computer per il computer locale.
2.  Usare tale DN per eseguire l'associazione all'oggetto computer e creare il SCP.

Per altre informazioni e un esempio di codice, vedere [Come i client trovano e usano un punto di connessione del servizio.](how-clients-find-and-use-a-service-connection-point.md)

Tenere presente che solo i computer membri del dominio hanno oggetti computer validi nella directory .

Per ottenere il nome DNS o NetBIOS del computer locale, chiamare la [**funzione GetComputerNameEx.**](/windows/desktop/api/sysinfoapi/nf-sysinfoapi-getcomputernameexa)

 

 