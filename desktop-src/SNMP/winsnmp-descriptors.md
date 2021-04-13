---
title: Descrittori WinSNMP
description: Nell'ambiente di programmazione WinSNMP, un descrittore è una delle due strutture seguenti.
ms.assetid: a329963b-cdb9-40d2-9a82-6f0d9f4ac73a
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8cd7f844ab1365d6020afce0ca7bfeb3afa244a8
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104328804"
---
# <a name="winsnmp-descriptors"></a>Descrittori WinSNMP

Nell'ambiente di programmazione WinSNMP, un *descrittore* è una delle due strutture seguenti:

-   Struttura [**smiOCTETS**](/windows/desktop/api/Winsnmp/ns-winsnmp-smioctets) che descrive una variabile di stringa ottetto
-   Struttura [**smiOID**](/windows/desktop/api/Winsnmp/ns-winsnmp-smioid) che descrive una variabile dell'identificatore di oggetto SNMP

Un descrittore WinSNMP è una struttura con due membri: un membro length, **Len** e un membro puntatore, **ptr**. Il membro **ptr** punta alla stringa ottetto o all'identificatore di oggetto di interesse. Il membro **ptr** può essere il tipo di dati **smiLPBYTE** o **smiLPUINT32** .

Un descrittore [**smiOCTETS**](/windows/desktop/api/Winsnmp/ns-winsnmp-smioctets) o un descrittore [**smiOID**](/windows/desktop/api/Winsnmp/ns-winsnmp-smioid) può essere il membro del **valore** di una struttura **smiVALUE** . La struttura [**smiVALUE**](/windows/desktop/api/Winsnmp/ns-winsnmp-smivalue) descrive il valore associato a un nome di variabile in una voce di binding variabile.

L'implementazione di Microsoft WinSNMP alloca e dealloca la memoria per tutte le strutture di output **smiOCTETS** e **smiOID** . Pertanto, l'applicazione deve chiamare la funzione [**SnmpFreeDescriptor**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpfreedescriptor) per liberare la memoria per il membro **ptr** di queste strutture.

I membri di stringa nei descrittori non richiedono un byte di terminazione **null** . Per ulteriori informazioni sulla gestione della memoria allocata per i descrittori, vedere [allocazione di oggetti memoria WinSNMP](allocating-winsnmp-memory-objects.md).

 

 




