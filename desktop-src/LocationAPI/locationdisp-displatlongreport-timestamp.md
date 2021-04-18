---
description: Data e ora in cui è stato generato il report.
ms.assetid: 3b8036aa-499c-4baf-bcc4-5b6c3f54eb7b
title: Proprietà LocationDisp. DispLatLongReport. timestamp
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- LocationDisp.DispLatLongReport.Timestamp
api_type:
- COM
api_location: ''
ms.openlocfilehash: 5ec179c5958b1be73a5fd5f74e48d0063edb6696
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106319034"
---
# <a name="locationdispdisplatlongreporttimestamp-property"></a>Proprietà LocationDisp. DispLatLongReport. timestamp

\[Il modello a oggetti dell'API location è disponibile per l'uso nei sistemi operativi specificati nella sezione requisiti. È possibile che in versioni successive sia stata modificata o non sia più disponibile. Per accedere al percorso da un sito Web, usare invece l' [API di georilevazione W3C](/previous-versions/windows/internet-explorer/ie-developer/samples/gg589513(v=vs.85)). Per accedere alla posizione da un'applicazione desktop, usare l'API [**Windows. Devices. Geolocation**](/uwp/api/Windows.Devices.Geolocation) .\]

Data e ora in cui è stato generato il report.

Questa proprietà è di sola lettura.

## <a name="syntax"></a>Sintassi


```JScript
Timestamp = LocationDisp.DispLatLongReport.Timestamp
```



## <a name="property-value"></a>Valore proprietà

Questa proprietà è una **Data** di sola lettura. I timestamp vengono forniti come ora UTC (Coordinated Universal Time).

## <a name="remarks"></a>Commenti

Si noti che per i linguaggi di scripting, ad esempio Microsoft JScript, potrebbe essere necessario eseguire conversioni in altri formati di tempo quando si visualizzano i timestamp come stringhe.

## <a name="examples"></a>Esempio

Per un esempio di come usare questa proprietà, vedere [un semplice esempio di report LatLong](/uwp/api/Windows.Devices.Geolocation).

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|--------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows 7\]<br/> |
| Server minimo supportato<br/> | Nessuno supportato<br/>                  |



 

