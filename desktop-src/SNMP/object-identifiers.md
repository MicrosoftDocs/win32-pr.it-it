---
title: Identificatori di oggetto (SNMP)
description: Un identificatore di oggetto SNMP assegna un nome univoco a un oggetto e ne identifica la posizione all'interno di una struttura ad albero MIB (Management Information Base).
ms.assetid: b4552185-ef37-4e04-9b19-a226165e0b32
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3ed1f54f67b85000e508dddb42b9c784628a53ab
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/10/2020
ms.locfileid: "103739330"
---
# <a name="object-identifiers-snmp"></a>Identificatori di oggetto (SNMP)

Un identificatore di oggetto SNMP assegna un nome univoco a un oggetto e ne identifica la posizione all'interno di una struttura ad albero MIB (Management Information Base). Gli identificatori di oggetto sono tipi di dati (ASN. 1) indipendenti dall'applicazione che sono costituiti da una sequenza di numeri interi non negativi o sottoidentificatori. Gli identificatori di oggetto devono avere un minimo di due sottoidentificatori e non devono superare 128 sottoidentificatori.

L'ambiente di programmazione WinSNMP utilizza la struttura [**smiOID**](/windows/desktop/api/Winsnmp/ns-winsnmp-smioid) per gestire gli identificatori di oggetto. Il formato della matrice di identificatori di oggetto in una struttura **smiOID** è un sottoidentificatore per ogni elemento di matrice.

La rappresentazione di stringa numerica punteggiata di un identificatore di oggetto separa i relativi sottoidentificatori con i punti; ad esempio, "1.2.3.4.5.6".

Per ulteriori informazioni, vedere [SNMP Management Information Base (MIB)](the-snmp-management-information-base-mib-.md) e le RFC pertinenti.

 

 




