---
description: La funzione QueryContextAttributes (digest) fornisce informazioni sulle impostazioni correnti di un contesto di sicurezza.
ms.assetid: 36863f1d-ed4e-40ec-8831-1f8b9918f2d8
title: Esecuzione di query sugli attributi del contesto di sicurezza digest
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 526c9e496a986f61762e663422a9d1eb939b1376
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103967396"
---
# <a name="querying-digest-security-context-attributes"></a>Esecuzione di query sugli attributi del contesto di sicurezza digest

La funzione [**QueryContextAttributes (digest)**](/windows/win32/api/rrascfg/nn-rrascfg-ieapproviderconfig) fornisce informazioni sulle impostazioni correnti di un [*contesto di sicurezza*](../secgloss/s-gly.md).

Microsoft Digest supporta l'esecuzione di query sui seguenti attributi del contesto di sicurezza.



| Attributo                   | Descrizione                                                                                                                                                                                             |
|-----------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| \_informazioni sulla \_ chiave SECPKG attr \_     | Informazioni relative agli algoritmi di firma e crittografia in uso.                                                                                                                                   |
| \_informazioni sul \_ pacchetto SECPKG attr \_ | Informazioni generali relative all'Microsoft Digest, ad esempio le dimensioni massime del token consentite dal [*pacchetto di sicurezza*](../secgloss/s-gly.md). |
| \_dimensioni attr \_ SECPKG         | Dimensioni massime consentite per i dati correlati al messaggio, ad esempio le firme.                                                                                                                                |



 

 

 
