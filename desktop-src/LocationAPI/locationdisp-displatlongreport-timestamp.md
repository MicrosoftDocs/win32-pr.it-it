---
description: 'Proprietà LocationDisp.DispLatLongReport.Timestamp : data e ora di generazione del report.'
ms.assetid: 3b8036aa-499c-4baf-bcc4-5b6c3f54eb7b
title: Proprietà LocationDisp.DispLatLongReport.Timestamp
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
ms.openlocfilehash: 02b1d2bc344ec954f8c309e2370755464857fd754b16f6664760f9df4e0e5f54
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120129911"
---
# <a name="locationdispdisplatlongreporttimestamp-property"></a>Proprietà LocationDisp.DispLatLongReport.Timestamp

\[Il modello a oggetti dell'API Location è disponibile per l'uso nei sistemi operativi specificati nella sezione Requisiti. È possibile che in versioni successive sia stata modificata o non sia più disponibile. Per accedere invece alla posizione da un sito Web, usare [l'API di georilevazione W3C](/previous-versions/windows/internet-explorer/ie-developer/samples/gg589513(v=vs.85)). Per accedere alla posizione da un'applicazione desktop, usare il [**Windows. API Devices.Geolocation.**](/uwp/api/Windows.Devices.Geolocation)\]

Data e ora di generazione del report.

Questa proprietà è di sola lettura.

## <a name="syntax"></a>Sintassi


```JScript
Timestamp = LocationDisp.DispLatLongReport.Timestamp
```



## <a name="property-value"></a>Valore proprietà

Questa proprietà è una data di sola **lettura.** I timestamp vengono forniti come Coordinated Universal Time (UTC).

## <a name="remarks"></a>Commenti

Si noti che i linguaggi di scripting, ad esempio Microsoft JScript, potrebbero richiedere l'esecuzione di conversioni in altri formati di ora quando si visualizzano timestamp come stringhe.

## <a name="examples"></a>Esempio

Per un esempio di come usare questa proprietà, vedere [Esempio di report LatLong semplice.](/uwp/api/Windows.Devices.Geolocation)

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|--------------------------------------------|
| Client minimo supportato<br/> | Windows 7 \[ app desktop\]<br/> |
| Server minimo supportato<br/> | Nessuno supportato<br/>                  |



 

