---
description: L'API di Gestione identità peer consente di creare, enumerare e modificare le identità peer in un'applicazione peer.
ms.assetid: c1b2a587-71c7-4623-a318-4624dad7feba
title: Informazioni su Identity Manager
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0d062f7324bb949c657b7687b533058cb9e74d3102eea1e484284453d3ff7f25
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119579921"
---
# <a name="about-identity-manager"></a>Informazioni su Identity Manager

L'API di Gestione identità peer consente di creare, enumerare e modificare le identità peer in un'applicazione peer. È possibile usare le identità peer create usando questa API come input per le API del provider dello spazio dei nomi PNRP (Peer Grouping and Peer Name Resolution Protocol).

## <a name="peer-identity-manager-best-practices"></a>Procedure consigliate per Peer Identity Manager

Ogni utente deve avere alcune identità peer che può usare per le attività peer. Ad esempio, un utente potrebbe avere due identità peer per lavoro e per lavoro.

Un'applicazione peer ben progettata consente a un utente di selezionare un'identità peer da usare. Un utente può creare una nuova identità peer se nessuna delle identità peer esistenti è appropriata per l'uso con un'applicazione.

Un'applicazione peer ben progettata controlla anche il numero di identità create. Se un'applicazione crea un'identità peer temporanea, l'applicazione deve eliminare l'identità peer quando l'identità non è necessaria. Se un'applicazione non esegue questa manutenzione, Gestione identità peer potrebbe non essere in grado di creare identità peer fino a quando non vengono rimosse alcune identità peer.

 

 



