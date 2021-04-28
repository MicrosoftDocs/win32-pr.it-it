---
description: 'Proprietà LocationDisp.DispCivicAddressReport.Timestamp : data e ora di generazione del report.'
ms.assetid: b9435384-72e0-42c4-a948-df52621a5ec2
title: Proprietà LocationDisp.DispCivicAddressReport.Timestamp
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- LocationDisp.DispCivicAddressReport.Timestamp
api_type:
- COM
api_location: ''
ms.openlocfilehash: d2ed39956bb542aa4e150bf9afa3e59a472a4d91
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/28/2021
ms.locfileid: "108110879"
---
# <a name="locationdispdispcivicaddressreporttimestamp-property"></a>Proprietà LocationDisp.DispCivicAddressReport.Timestamp

\[Il modello a oggetti dell'API Location è disponibile per l'uso nei sistemi operativi specificati nella sezione Requisiti. È possibile che in versioni successive sia stata modificata o non sia più disponibile. Per accedere invece alla posizione da un sito Web, usare [l'API di georilevazione W3C](/previous-versions/windows/internet-explorer/ie-developer/samples/gg589513(v=vs.85)). Per accedere alla posizione da un'applicazione desktop, usare l'API [**Windows.Devices.Geolocation.**](/uwp/api/Windows.Devices.Geolocation)\]

Data e ora di generazione del report.

Questa proprietà è di sola lettura.

## <a name="syntax"></a>Sintassi


```JScript
Timestamp = LocationDisp.DispCivicAddressReport.Timestamp
```



## <a name="property-value"></a>Valore proprietà

Questa proprietà è una data di sola **lettura.** I timestamp vengono forniti come Coordinated Universal Time (UTC).

## <a name="remarks"></a>Commenti

Si noti che i linguaggi di scripting, ad esempio Microsoft JScript, potrebbero richiedere l'esecuzione di conversioni in altri formati di ora quando si visualizzano timestamp come stringhe.

## <a name="examples"></a>Esempio

Per un esempio di come usare questa proprietà, vedere [a Simple Civic Address Report Example](/uwp/api/Windows.Devices.Geolocation).

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|--------------------------------------------|
| Client minimo supportato<br/> | Solo app desktop di Windows 7 \[\]<br/> |
| Server minimo supportato<br/> | Nessuno supportato<br/>                  |



 

