---
description: XML è uno standard di settore per la descrizione dei dati strutturati. Una firma digitale XML è una rappresentazione XML di una firma digitale che offre la possibilità di verificare l'origine e l'integrità del documento XML e i dati a cui si fa riferimento esternamente.
ms.assetid: 02ca8d9b-be08-4b15-895f-9c8c4b0ed536
title: Cenni preliminari sulla firma digitale XML
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b41a1b748305ab26b686e126cd201ad9e7f34d51
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106312777"
---
# <a name="xml-digital-signature-overview"></a>Cenni preliminari sulla firma digitale XML

XML è uno standard di settore per la descrizione dei dati strutturati. Una firma digitale XML è una rappresentazione XML di una [*firma digitale*](../secgloss/d-gly.md) che offre la possibilità di verificare l'origine e l'integrità del documento XML e i dati a cui si fa riferimento esternamente. Le firme digitali XML possono essere utilizzate per firmare dati arbitrari, inclusi un documento o un frammento XML, una pagina HTML, testo normale o dati con codifica binaria, ad esempio un file JPEG.

Il formato di firma digitale XML supportato dall'API CryptXML Digital Signature viene specificato dalla raccomandazione W3C XML Signature Syntax and Processing (Second Edition).

La firma digitale CryptXML implementa il supporto per i tipi di firma richiesti, gli algoritmi di crittografia, gli algoritmi di canonizzazione e la trasformazione busta specificata.

Gli sviluppatori possono estendere il set predefinito di algoritmi di crittografia supportati da CryptXML creando dll di estensioni crittografiche. Gli sviluppatori possono anche creare le proprie trasformazioni e gli algoritmi di canonizzazione personalizzati sull'API CryptXML. Gli sviluppatori possono usare le API CryptXML con le API di Windows Certificate.

 

 
