---
description: WMI attualmente non supporta il codice gestito in WMI, ma è supportato nell'istanza gestita.
ms.assetid: ED6EF216-7FF7-45F2-9FDD-3A73D5F65F9B
ms.tgt_platform: multiple
title: Creazione di un client WMI gestito
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 6f28b01cb3b4506e0b47332cc3336af95dd641e78c7716f33b8e62b162081bdd
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120071521"
---
# <a name="creating-a-managed-wmi-client"></a>Creazione di un client WMI gestito

La versione corrente di WMI contiene lo spazio dei nomi System.Management, che espone una serie di API che interagiscono con WMI. Tuttavia, non è consigliabile usare questo spazio dei nomi.

Se si vuole creare un client WMI gestito, è consigliabile usare Windows Management Infrastructure (MI). MI è la versione di nuova generazione di WMI e contiene il supporto completo per il codice gestito. Per altre informazioni, vedere [How to Implement a Managed MI Client](/previous-versions/windows/desktop/wmi_v2/how-to-implement-a-managed-mi-client).

 

 
