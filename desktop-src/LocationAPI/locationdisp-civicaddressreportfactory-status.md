---
description: Stato corrente del report.
ms.assetid: 3aae0b61-cdaa-4131-b6e1-406813bb1848
title: Proprietà LocationDisp. CivicAddressReportFactory. status
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
ms.openlocfilehash: ff937b11fbb64e0ec1596f9b3b9d85b33528eb06
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106319037"
---
# <a name="locationdispcivicaddressreportfactorystatus-property"></a>Proprietà LocationDisp. CivicAddressReportFactory. status

\[Il modello a oggetti dell'API location è disponibile per l'uso nei sistemi operativi specificati nella sezione requisiti. È possibile che in versioni successive sia stata modificata o non sia più disponibile. Per accedere al percorso da un sito Web, usare invece l' [API di georilevazione W3C](/previous-versions/windows/internet-explorer/ie-developer/samples/gg589513(v=vs.85)). Per accedere alla posizione da un'applicazione desktop, usare l'API [**Windows. Devices. Geolocation**](/uwp/api/Windows.Devices.Geolocation) .\]

Stato corrente del report.

Questa proprietà è di sola lettura.

## <a name="syntax"></a>Sintassi


```JScript
Status = LocationDisp.CivicAddressReportFactory.Status
```



## <a name="property-value"></a>Valore proprietà

Questa proprietà è un **numero** di sola lettura (unsigned long).



| Stato                                                                                               | Significato                          |
|------------------------------------------------------------------------------------------------------|----------------------------------|
| <span id="0"></span><dl> <dt>**0**</dt> </dl> | Il report non è supportato.<br/> |
| <span id="1"></span><dl> <dt>**1**</dt> </dl> | Errore.<br/>                |
| <span id="2"></span><dl> <dt>**2**</dt> </dl> | Accesso negato.<br/>        |
| <span id="3"></span><dl> <dt>**3**</dt> </dl> | Inizializzazione.<br/>         |
| <span id="4"></span><dl> <dt>**4**</dt> </dl> | In esecuzione.<br/>              |



 

## <a name="examples"></a>Esempio

Per un esempio di come usare questa proprietà, vedere [ascolto di eventi di report di indirizzi civici](/uwp/api/Windows.Devices.Geolocation).

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|--------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows 7\]<br/> |
| Server minimo supportato<br/> | Nessuno supportato<br/>                  |



 

