---
description: L'API peer Identity Manager consente di creare, enumerare e modificare le identità dei peer in un'applicazione peer.
ms.assetid: c1b2a587-71c7-4623-a318-4624dad7feba
title: Informazioni su Identity Manager
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dfe66e21bf6c131006ed98c7f5f211c316464ebe
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103881818"
---
# <a name="about-identity-manager"></a>Informazioni su Identity Manager

L'API peer Identity Manager consente di creare, enumerare e modificare le identità dei peer in un'applicazione peer. È possibile utilizzare le identità peer create utilizzando questa API come input per il raggruppamento peer e le API del provider dello spazio dei nomi PNRP (Peer Name Resolution Protocol).

## <a name="peer-identity-manager-best-practices"></a>Procedure consigliate per peer Identity Manager

Ogni utente deve avere alcune identità peer che possono usare per le attività peer. Ad esempio, un utente potrebbe avere due identità peer per lavoro e svago.

Un'applicazione peer ben progettata consente a un utente di selezionare un'identità peer da usare. Un utente può creare una nuova identità peer se nessuna delle identità peer esistenti è appropriata per l'uso con un'applicazione.

Un'applicazione peer ben progettata controlla anche il numero di identità create. Se un'applicazione crea un'identità peer temporanea, l'applicazione deve eliminare l'identità peer quando l'identità non è necessaria. Se un'applicazione non esegue questa manutenzione, il gestore di identità peer potrebbe non essere in grado di creare identità peer finché alcune identità peer non vengono rimosse.

 

 



