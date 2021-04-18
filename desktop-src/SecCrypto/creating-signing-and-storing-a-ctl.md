---
description: Creare un elenco certificati attendibili (CTL) firmato e salvarlo in un archivio certificati.
ms.assetid: 82d75d60-2343-413c-ba53-ccee02d1ad41
title: Creazione, firma e archiviazione di un elenco di scopi consentiti
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2da66ce5acb882d36451118700178519455a4ded
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106306469"
---
# <a name="creating-signing-and-storing-a-ctl"></a>Creazione, firma e archiviazione di un elenco di scopi consentiti

Le procedure seguenti creano un [*elenco certificati attendibili*](../secgloss/c-gly.md) (CTL) firmato e lo salvano in un [*archivio certificati*](../secgloss/c-gly.md).

**Per creare e firmare un elenco di scopi consentiti**

1.  Creare una matrice di elementi da archiviare nell' [*elenco*](../secgloss/c-gly.md)di scopi consentiti. Nel caso di certificati attendibili, devono essere gli hash SHA1 o MD5 dei certificati attendibili.
2.  Inizializzare una struttura di [**\_ informazioni CTL**](/windows/desktop/api/Wincrypt/ns-wincrypt-ctl_info) che includa la matrice di elementi appena creati.
3.  Inizializza una struttura di [**\_ informazioni di \_ codifica \_ CMSG firmata**](/windows/desktop/api/Wincrypt/ns-wincrypt-cmsg_signed_encode_info) .
4.  Chiamare [**CryptMsgEncodeAndSignCTL**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptmsgencodeandsignctl). Questa chiamata di funzione restituisce un puntatore a un elenco di scopi consentiti codificato (in \# formato PKCS 7) che contiene l'elenco di elementi creati nel passaggio 1.

**Per aggiungere un elenco di scopi consentiti a un archivio certificati**

1.  Ottenere un puntatore a un elenco di scopi consentiti firmato e codificato.
2.  Aprire l'archivio certificati di destinazione con una chiamata a [**CertOpenStore**](/windows/desktop/api/Wincrypt/nf-wincrypt-certopenstore).
3.  Chiamare [**CertAddEncodedCTLToStore**](/windows/desktop/api/Wincrypt/nf-wincrypt-certaddencodedctltostore).

 

 
