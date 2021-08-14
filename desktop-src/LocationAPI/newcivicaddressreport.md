---
description: Si verifica quando viene generato un nuovo report degli indirizzi civici.
ms.assetid: a8df870e-6744-4e8a-a103-56b446da135f
title: Evento NewCivicAddressReport
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- NewCivicAddressReport
api_type:
- COM
api_location: ''
ms.openlocfilehash: 61b5c6c05d8aa551148d278fa0cbafa8791bbc4c1a1f6b1142ef7f2ef80af318
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118386739"
---
# <a name="newcivicaddressreport-event"></a>Evento NewCivicAddressReport

\[Il modello a oggetti dell'API Location è disponibile per l'uso nei sistemi operativi specificati nella sezione Requisiti. È possibile che in versioni successive sia stata modificata o non sia più disponibile. Per accedere invece alla posizione da un sito Web, usare [l'API di georilevazione W3C](/previous-versions/windows/internet-explorer/ie-developer/samples/gg589513(v=vs.85)). Per accedere alla posizione da un'applicazione desktop, usare il [**Windows. API Devices.Geolocation.**](/uwp/api/Windows.Devices.Geolocation)\]

Si verifica quando viene generato un nuovo report degli indirizzi civici.

## <a name="syntax"></a>Sintassi


```JScript
.NewCivicAddressReport(
  newReport
)
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*newReport* 
</dt> <dd>

Nuovo [**oggetto LocationDisp.DispCivicAddressReport.**](locationdisp-dispcivicaddressreport.md)

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Questo evento non restituisce un valore.

## <a name="examples"></a>Esempio

Per un esempio di come usare questo evento, vedere [Listening for Civic Address Report Events](/uwp/api/Windows.Devices.Geolocation).

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|--------------------------------------------|
| Client minimo supportato<br/> | Windows 7 \[ app desktop\]<br/> |
| Server minimo supportato<br/> | Nessuno supportato<br/>                  |



 

