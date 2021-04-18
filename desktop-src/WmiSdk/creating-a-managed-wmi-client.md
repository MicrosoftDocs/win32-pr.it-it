---
description: WMI attualmente non supporta il codice gestito in WMI, ma è supportato in MI.
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
ms.openlocfilehash: bb1339347c4e15cd29ebf4d4e98e5a8b61a24e97
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106310395"
---
# <a name="creating-a-managed-wmi-client"></a>Creazione di un client WMI gestito

La versione corrente di WMI contiene lo spazio dei nomi System. Management, che espone un numero di API che interagiscono con WMI. Tuttavia, non è consigliabile usare questo spazio dei nomi.

Se si desidera creare un client WMI gestito, è consigliabile utilizzare Windows Management Infrastructure (MI). MI è la versione di nuova generazione di WMI e contiene il supporto completo per il codice gestito. Per ulteriori informazioni, vedere [come implementare un client mi gestito](/previous-versions/windows/desktop/wmi_v2/how-to-implement-a-managed-mi-client).

 

 
