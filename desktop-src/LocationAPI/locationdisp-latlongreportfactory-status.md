---
description: 'Proprietà LocationDisp.LatLongReportFactory.Status : stato del report corrente.'
ms.assetid: bcdf76b5-88c4-481a-89ac-2b9558cecfc0
title: Proprietà LocationDisp.LatLongReportFactory.Status
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- LocationDisp.LatLongReportFactory.Status
api_type:
- COM
api_location: ''
ms.openlocfilehash: 37e66c3f289f5376b31ffe516f45d79f2fef51e2
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/28/2021
ms.locfileid: "108088899"
---
# <a name="locationdisplatlongreportfactorystatus-property"></a>Proprietà LocationDisp.LatLongReportFactory.Status

\[Il modello a oggetti dell'API Location è disponibile per l'uso nei sistemi operativi specificati nella sezione Requisiti. È possibile che in versioni successive sia stata modificata o non sia più disponibile. Per accedere invece alla posizione da un sito Web, usare [l'API di georilevazione W3C](/previous-versions/windows/internet-explorer/ie-developer/samples/gg589513(v=vs.85)). Per accedere alla posizione da un'applicazione desktop, usare l'API [**Windows.Devices.Geolocation.**](/uwp/api/Windows.Devices.Geolocation)\]

Stato del report corrente.

Questa proprietà è di sola lettura.

## <a name="syntax"></a>Sintassi


```JScript
Status = LocationDisp.LatLongReportFactory.Status
```



## <a name="property-value"></a>Valore proprietà

Questa proprietà è un numero di sola **lettura** (unsigned long).



| Stato                                                                                               | Significato                          |
|------------------------------------------------------------------------------------------------------|----------------------------------|
| <span id="0"></span><dl> <dt>**0**</dt> </dl> | Report non supportato.<br/> |
| <span id="1"></span><dl> <dt>**1**</dt> </dl> | Errore.<br/>                |
| <span id="2"></span><dl> <dt>**2**</dt> </dl> | Accesso negato.<br/>        |
| <span id="3"></span><dl> <dt>**3**</dt> </dl> | Inizializzazione.<br/>         |
| <span id="4"></span><dl> <dt>**4**</dt> </dl> | In esecuzione.<br/>              |



 

## <a name="examples"></a>Esempio

Per un esempio di come usare questa proprietà, vedere [Listening for LatLong Report Events](/uwp/api/Windows.Devices.Geolocation).

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|--------------------------------------------|
| Client minimo supportato<br/> | Solo app desktop di Windows 7 \[\]<br/> |
| Server minimo supportato<br/> | Nessuno supportato<br/>                  |



 

