---
title: Callback degli avvisi RPF
description: Dopo che il gestore di gruppi multicast riceve la notifica di un pacchetto da una nuova origine o di un pacchetto destinato a un nuovo gruppo, il gestore di gruppi multicast cerca la route all'origine nella visualizzazione multicast della tabella di routing.
ms.assetid: dacccca2-e6a5-417a-a217-06ff846d55f0
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8ff1c2dc66b2307b60fb649fd8a0adb6992a63532bf9aa45350d261ab04b6c5d
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120035921"
---
# <a name="rpf-alert-callbacks"></a>Callback degli avvisi RPF

Dopo che il gestore di gruppi multicast riceve la notifica di un pacchetto da una nuova origine o di un pacchetto destinato a un nuovo gruppo, il gestore di gruppi multicast cerca la route all'origine nella visualizzazione multicast della tabella di routing. Il gestore del gruppo multicast richiama quindi il callback [**\_ RPF \_ CALLBACK PMGM**](/windows/desktop/api/Mgm/nc-mgm-pmgm_rpf_callback) al protocollo proprietario dell'interfaccia su cui sono arrivati i dati.

Dopo aver richiamato questo callback, il protocollo di routing può modificare l'interfaccia in ingresso se il protocollo di routing deve ricevere i dati per il gruppo in un'interfaccia diversa.

 

 




