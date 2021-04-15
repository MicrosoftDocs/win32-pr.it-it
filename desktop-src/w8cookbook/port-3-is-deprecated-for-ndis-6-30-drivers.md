---
title: La porta 3 è deprecata per i driver NDIS 6,30
description: La porta 3 è deprecata per i driver NDIS 6,30
ms.assetid: 900BD08D-3EAF-43F3-A74A-359815474FAD
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: df0b4c7f6a33b179a14d3d7f8151d3850e16dd44
ms.sourcegitcommit: ea4baf9953a78d2d6bd530b680601e39f3884541
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/01/2020
ms.locfileid: "104474494"
---
# <a name="port-3-is-deprecated-for-ndis-630-drivers"></a>La porta 3 è deprecata per i driver NDIS 6,30

## <a name="platforms"></a>Piattaforme

**Client** -Windows 8  
**Server** : Windows Server 2012  


## <a name="description"></a>Descrizione

Windows 8 rimuove il supporto della piattaforma per i driver WLAN miniport NDIS per creare o avviare la porta di estendibilità IHV (nota anche come terza porta). Questa funzionalità è stata introdotta in Windows 7 come misura tampone mentre Wi-Fi Alliance (WFA) ha sviluppato la specifica Wi-Fi diretta. La specifica è ora terminata, i prodotti che usano Wi-Fi Direct vengono certificati e Windows 8 introduce uno stack nativo Wi-Fi diretto.

## <a name="manifestation"></a>Manifestazione

Niente, perché la terza porta è una funzionalità della piattaforma che i driver miniport di rete WLAN si avviano se questa funzionalità è necessaria.

## <a name="solution"></a>Soluzione

La funzionalità della porta di estendibilità è disponibile per i driver esistenti che non segnalano NDIS 6,30 per garantire la compatibilità dei dispositivi. Tuttavia, i nuovi driver WLAN che segnalano NDIS 6,30 non saranno in grado di avviare la porta. gli sviluppatori di questi driver devono invece usare Wi-Fi Direct.

 

 




