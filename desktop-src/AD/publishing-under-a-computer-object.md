---
title: Pubblicazione in un oggetto computer
description: In genere, i servizi basati su host creano convergenza nell'oggetto computer per il computer host. I servizi basati su host sono strettamente legati a un singolo computer host.
ms.assetid: ecd7d8bc-4714-408a-856c-7cab8360bf81
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 77fe382001910f3b78b4461c622e94b14c54fb59
ms.sourcegitcommit: 803f3ccd65bdefe36bd851b9c6e7280be9489016
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/17/2020
ms.locfileid: "103872266"
---
# <a name="publishing-under-a-computer-object"></a>Pubblicazione in un oggetto computer

In genere, i servizi basati su host creano convergenza nell'oggetto computer per il computer host. I servizi basati su host sono strettamente legati a un singolo computer host.

**Per creare convergenza in un oggetto computer**

1.  Chiamare la funzione [**GetComputerObjectName**](/windows/desktop/api/secext/nf-secext-getcomputerobjectnamea) per ottenere il nome distinto (DN) nella directory dell'oggetto computer per il computer locale.
2.  Usare tale DN per eseguire l'associazione all'oggetto computer e creare SCP.

Per ulteriori informazioni e un esempio di codice, vedere [modalità di individuazione e utilizzo di un punto di connessione del servizio](how-clients-find-and-use-a-service-connection-point.md)da parte dei client.

Tenere presente che nella directory solo i computer membri del dominio dispongono di oggetti computer validi.

Per ottenere il nome DNS o NetBIOS del computer locale, chiamare la funzione [**presunto GetComputerNameEx**](/windows/desktop/api/sysinfoapi/nf-sysinfoapi-getcomputernameexa) .

 

 