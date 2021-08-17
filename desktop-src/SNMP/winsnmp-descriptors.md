---
title: Descrittori WinSNMP
description: Nell'ambiente di programmazione WinSNMP un descrittore è una delle due strutture seguenti.
ms.assetid: a329963b-cdb9-40d2-9a82-6f0d9f4ac73a
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 875112d8519f93f4b5ae6729401f2689294a84c55dc729f0ffa24d05076e300b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119142914"
---
# <a name="winsnmp-descriptors"></a>Descrittori WinSNMP

Nell'ambiente di programmazione WinSNMP un *descrittore* è una delle due strutture seguenti:

-   Struttura [**smiOCTETS**](/windows/desktop/api/Winsnmp/ns-winsnmp-smioctets) che descrive una variabile stringa ottetto
-   Struttura [**smiOID**](/windows/desktop/api/Winsnmp/ns-winsnmp-smioid) che descrive una variabile identificatore di oggetto SNMP

Un descrittore WinSNMP è una struttura con due membri: un membro di lunghezza, **len** e un membro puntatore, **ptr**. Il **membro ptr** punta alla stringa dell'ottetto o all'identificatore di oggetto di interesse. Il **membro ptr** può essere il tipo di dati **smiLPBYTE** o **smiLPUINT32.**

Un [**descrittore smiOCTETS**](/windows/desktop/api/Winsnmp/ns-winsnmp-smioctets) o un descrittore [**smiOID**](/windows/desktop/api/Winsnmp/ns-winsnmp-smioid) può essere il membro **valore** di una **struttura smiVALUE.** La [**struttura smiVALUE**](/windows/desktop/api/Winsnmp/ns-winsnmp-smivalue) descrive il valore associato a un nome di variabile in una voce di associazione di variabili.

L'implementazione Microsoft WinSNMP alloca e dealloca la memoria per tutte le strutture **smiOCTETS** e **smiOID di** output. Pertanto, l'applicazione deve chiamare la [**funzione SnmpFreeDescriptor**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpfreedescriptor) per liberare la memoria per il membro **ptr** di queste strutture.

I membri stringa nei descrittori non richiedono un byte di terminazione **NULL.** Per altre informazioni sulla gestione della memoria allocata per i descrittori, vedere [Allocazione di oggetti di memoria WinSNMP](allocating-winsnmp-memory-objects.md).

 

 




