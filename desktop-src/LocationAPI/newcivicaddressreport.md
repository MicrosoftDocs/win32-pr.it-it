---
description: Si verifica quando viene generato un nuovo report sull'indirizzo civico.
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
ms.openlocfilehash: fa786ecee4ce4223cdb7ec0c8400c5c11bf6e192
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "103885534"
---
# <a name="newcivicaddressreport-event"></a>Evento NewCivicAddressReport

\[Il modello a oggetti dell'API location è disponibile per l'uso nei sistemi operativi specificati nella sezione requisiti. È possibile che in versioni successive sia stata modificata o non sia più disponibile. Per accedere al percorso da un sito Web, usare invece l' [API di georilevazione W3C](/previous-versions/windows/internet-explorer/ie-developer/samples/gg589513(v=vs.85)). Per accedere alla posizione da un'applicazione desktop, usare l'API [**Windows. Devices. Geolocation**](/uwp/api/Windows.Devices.Geolocation) .\]

Si verifica quando viene generato un nuovo report sull'indirizzo civico.

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

Nuovo oggetto [**LocationDisp. DispCivicAddressReport**](locationdisp-dispcivicaddressreport.md) .

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Questo evento non restituisce un valore.

## <a name="examples"></a>Esempio

Per un esempio di come usare questo evento, vedere [ascolto di eventi di report di indirizzi civici](/uwp/api/Windows.Devices.Geolocation).

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|--------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows 7\]<br/> |
| Server minimo supportato<br/> | Nessuno supportato<br/>                  |



 

