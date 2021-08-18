---
title: Installazione EAP
description: I fornitori implementano EAP, noti anche come protocolli di autenticazione, nelle librerie a collegamento dinamico (DLL).
ms.assetid: af10b1e9-45c9-4640-ba79-fc9c23cc3c47
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f9a790f4282ef2658bacdd7f25be647234c3cf32d62ca80e8ce2745da3f4f738
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118984451"
---
# <a name="eap-installation"></a>Installazione EAP

I fornitori implementano EAP, noti anche come protocolli di autenticazione, nelle librerie a collegamento dinamico (DLL). Una DLL per il protocollo di autenticazione deve risiedere nei computer client e server. Per semplicità, le DLL client e server possono essere identiche. Tuttavia, questo non è un requisito. Tenere inoltre presente che la stessa DLL può supportare più di un protocollo di autenticazione.

Il fornitore deve fornire il software di installazione per installare e rimuovere la DLL. Il software di installazione deve anche creare le chiavi e i valori appropriati per il protocollo di autenticazione nel Registro di sistema e rimuoverli al momento della disinstallazione.

L'installazione di ogni DLL EAP deve creare la chiave del Registro di sistema seguente.

**HKEY \_ Local \_ MACHINE** \\ **System** \\ **CurrentControlSet** \\ **Services** \\ **Rasman** \\ **PPP** \\ **EAP** \\ **&lt; eaptypeid &gt;**

Nel percorso precedente **&lt; eaptypeid &gt;** è l'ID del protocollo di autenticazione. Il fornitore deve ottenere questo ID dall'autorità IANA (Internet Assigned Numbers Authority).

Per altre informazioni e una descrizione dei valori supportati per questa chiave, vedere Valori del Registro di sistema del protocollo [di autenticazione](authentication-protocol-registry-values.md).

 

 




