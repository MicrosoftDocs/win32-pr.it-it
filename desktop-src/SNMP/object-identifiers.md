---
title: Identificatori di oggetto (SNMP)
description: Un identificatore di oggetto SNMP identifica in modo univoco un oggetto e ne identifica la posizione all'interno di una struttura ad albero MIB (Management Information Base).
ms.assetid: b4552185-ef37-4e04-9b19-a226165e0b32
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1b81d52e43cb3be89551dd597bc5084d533f3913264f8bcf5c0a2ef7dbb375bc
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119009259"
---
# <a name="object-identifiers-snmp"></a>Identificatori di oggetto (SNMP)

Un identificatore di oggetto SNMP identifica in modo univoco un oggetto e ne identifica la posizione all'interno di una struttura ad albero MIB (Management Information Base). Gli identificatori di oggetto sono tipi di dati ASN.1 (Abstract Syntax Notation One) indipendenti dall'applicazione che sono costituiti da una sequenza di interi non negativi o sottoidentificatori. Gli identificatori di oggetto devono avere almeno due sottoidentificatori e non devono superare 128 sottoidentificatori.

L'ambiente di programmazione WinSNMP usa la [**struttura smiOID**](/windows/desktop/api/Winsnmp/ns-winsnmp-smioid) per gestire gli identificatori di oggetto. Il formato della matrice di identificatori di oggetto in **una struttura smiOID** è un sottoidentificatore per ogni elemento della matrice.

La rappresentazione di stringa numerica tratteggiata di un identificatore di oggetto separa i relativi sottoidentificatori con punti. ad esempio "1.2.3.4.5.6".

Per altre informazioni, vedere [SNMP Management Information Base (MIB)](the-snmp-management-information-base-mib-.md) e le RFC pertinenti.

 

 




