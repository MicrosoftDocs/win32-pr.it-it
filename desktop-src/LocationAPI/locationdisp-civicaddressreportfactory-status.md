---
description: 'Proprietà LocationDisp.CivicAddressReportFactory.Status: stato del report corrente.'
ms.assetid: 3aae0b61-cdaa-4131-b6e1-406813bb1848
title: Proprietà LocationDisp.CivicAddressReportFactory.Status
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- LocationDisp.CivicAddressReportFactory.Status
api_type:
- COM
api_location: ''
ms.openlocfilehash: 8ba7d9e26a9741f80caed84d2a4ee4198eae05736aa8dee91019452cc3345ddf
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119693121"
---
# <a name="locationdispcivicaddressreportfactorystatus-property"></a>Proprietà LocationDisp.CivicAddressReportFactory.Status

\[Il modello a oggetti dell'API Location è disponibile per l'uso nei sistemi operativi specificati nella sezione Requisiti. È possibile che in versioni successive sia stata modificata o non sia più disponibile. Per accedere invece alla posizione da un sito Web, usare [l'API di georilevazione W3C](/previous-versions/windows/internet-explorer/ie-developer/samples/gg589513(v=vs.85)). Per accedere alla posizione da un'applicazione desktop, usare il [**Windows. API Devices.Geolocation.**](/uwp/api/Windows.Devices.Geolocation)\]

Stato corrente del report.

Questa proprietà è di sola lettura.

## <a name="syntax"></a>Sintassi


```JScript
Status = LocationDisp.CivicAddressReportFactory.Status
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

Per un esempio di come usare questa proprietà, vedere [Ascolto di eventi del report degli indirizzi civici](/uwp/api/Windows.Devices.Geolocation).

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|--------------------------------------------|
| Client minimo supportato<br/> | Windows 7 \[ app desktop\]<br/> |
| Server minimo supportato<br/> | Nessuno supportato<br/>                  |



 

