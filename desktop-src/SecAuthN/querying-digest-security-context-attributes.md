---
description: La funzione QueryContextAttributes (Digest) fornisce informazioni sulle impostazioni correnti di un contesto di sicurezza.
ms.assetid: 36863f1d-ed4e-40ec-8831-1f8b9918f2d8
title: Esecuzione di query su attributi del contesto di sicurezza digest
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 24499d5119814edec12f29cf5a39ea027f95c100626be1af1d132c952682599c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118919960"
---
# <a name="querying-digest-security-context-attributes"></a>Esecuzione di query su attributi del contesto di sicurezza digest

La [**funzione QueryContextAttributes (Digest)**](/windows/win32/api/rrascfg/nn-rrascfg-ieapproviderconfig) fornisce informazioni sulle impostazioni correnti di un contesto [*di sicurezza.*](../secgloss/s-gly.md)

Microsoft Digest supporta l'esecuzione di query nei seguenti attributi del contesto di sicurezza.



| Attributo                   | Descrizione                                                                                                                                                                                             |
|-----------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| INFORMAZIONI SULLA CHIAVE \_ SECPKG ATTR \_ \_     | Informazioni relative agli algoritmi di firma e crittografia in uso.                                                                                                                                   |
| INFORMAZIONI SUL PACCHETTO \_ SECPKG ATTR \_ \_ | Informazioni generali relative a Microsoft Digest, ad esempio la dimensione massima del token consentita dal pacchetto [*di sicurezza*](../secgloss/s-gly.md). |
| DIMENSIONI ATTR SECPKG \_ \_         | Dimensioni massime consentite per i dati correlati ai messaggi, ad esempio le firme.                                                                                                                                |



 

 

 
