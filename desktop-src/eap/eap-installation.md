---
title: Installazione EAP
description: I fornitori implementano EAPs, noti anche come protocolli di autenticazione, nelle librerie a collegamento dinamico (dll).
ms.assetid: af10b1e9-45c9-4640-ba79-fc9c23cc3c47
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 619505a55108ebde0e14d7ff20c78394c6c90fad
ms.sourcegitcommit: c20a43b333f03175ac23823c55f3204bfe8cd243
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 11/26/2019
ms.locfileid: "104398338"
---
# <a name="eap-installation"></a>Installazione EAP

I fornitori implementano EAPs, noti anche come protocolli di autenticazione, nelle librerie a collegamento dinamico (dll). Una DLL per il protocollo di autenticazione deve risiedere sia nei computer client che nei computer server. Per semplicità, le dll del client e del server possono essere identiche. Tuttavia, questo non è un requisito. Tenere inoltre presente che la stessa DLL può supportare più di un protocollo di autenticazione.

Il fornitore deve fornire il software di installazione per installare e rimuovere la DLL. Il software di installazione deve inoltre creare le chiavi e i valori appropriati per il protocollo di autenticazione nel registro di sistema e rimuoverli al momento della disinstallazione.

L'installazione di ogni DLL EAP deve creare la seguente chiave del registro di sistema.

**HKEY \_ \_Computer locale** \\ **sistema** \\ **CurrentControlSet** \\ **Servizi** \\ **RASMAN** \\ **PPP** \\ **EAP** \\ **&lt; eaptypeid &gt;**

Nel percorso precedente **&lt; eaptypeid &gt;** è l'ID del protocollo di autenticazione. Il fornitore deve ottenere questo ID da IANA (Internet Assigned Numbers Authority).

Per ulteriori informazioni e per una descrizione dei valori supportati per questa chiave, vedere [autenticazione del registro di sistema dei valori](authentication-protocol-registry-values.md).

 

 




