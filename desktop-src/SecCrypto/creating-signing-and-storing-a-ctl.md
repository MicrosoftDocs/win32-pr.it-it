---
description: Creare un elenco di certificati attendibili (CTL) firmato e salvarlo in un archivio certificati.
ms.assetid: 82d75d60-2343-413c-ba53-ccee02d1ad41
title: Creazione, firma e archiviazione di un CTL
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e3f9aac8c75f7c112a09c62bb52d6e554aee7703e7f3e02c101545de5c5196db
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119876561"
---
# <a name="creating-signing-and-storing-a-ctl"></a>Creazione, firma e archiviazione di un CTL

Nelle procedure seguenti viene creato un elenco di certificati [*attendibili*](../secgloss/c-gly.md) (CTL) firmato e salvato in un [*archivio certificati*](../secgloss/c-gly.md).

**Per creare e firmare un CTL**

1.  Creare una matrice di elementi da archiviare [*nell'elenco CTL.*](../secgloss/c-gly.md) Nel caso di certificati attendibili, questi devono essere gli hash SHA1 o MD5 dei certificati attendibili.
2.  Inizializzare una [**struttura CTL \_ INFO**](/windows/desktop/api/Wincrypt/ns-wincrypt-ctl_info) che include la matrice di elementi appena creati.
3.  Inizializzare [**una struttura CMSG \_ SIGNED \_ ENCODE \_ INFO.**](/windows/desktop/api/Wincrypt/ns-wincrypt-cmsg_signed_encode_info)
4.  Chiamare [**CryptMsgEncodeAndSignCTL**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptmsgencodeandsignctl). Questa chiamata di funzione restituisce un puntatore a un CTL con segno codificato (in formato PKCS 7) che contiene l'elenco di elementi \# creati nel passaggio 1.

**Per aggiungere un CTL a un archivio certificati**

1.  Ottenere un puntatore a un CTL firmato e codificato.
2.  Aprire l'archivio certificati di destinazione con una chiamata a [**CertOpenStore**](/windows/desktop/api/Wincrypt/nf-wincrypt-certopenstore).
3.  Chiamare [**CertAddEncodedCTLToStore**](/windows/desktop/api/Wincrypt/nf-wincrypt-certaddencodedctltostore).

 

 
