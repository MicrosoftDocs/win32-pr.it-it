---
description: Si verifica in seguito alla modifica dello stato operativo di un report.
ms.assetid: f0c4e678-1666-4f99-89de-85879eacd0ac
title: Evento StatusChanged
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- StatusChanged
api_type:
- COM
api_location: ''
ms.openlocfilehash: d1bda6645002f586eda0e2dad99a134450329d09
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104234357"
---
# <a name="statuschanged-event"></a>Evento StatusChanged

\[Il modello a oggetti dell'API location è disponibile per l'uso nei sistemi operativi specificati nella sezione requisiti. È possibile che in versioni successive sia stata modificata o non sia più disponibile. Per accedere al percorso da un sito Web, usare invece l' [API di georilevazione W3C](/previous-versions/windows/internet-explorer/ie-developer/samples/gg589513(v=vs.85)). Per accedere alla posizione da un'applicazione desktop, usare l'API [**Windows. Devices. Geolocation**](/uwp/api/Windows.Devices.Geolocation) .\]

Si verifica in seguito alla modifica dello stato operativo di un report.

## <a name="syntax"></a>Sintassi


```JScript
.StatusChanged(
  status
)
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*Stato* 
</dt> <dd>

Il nuovo stato.



| Stato                                                                                               | Significato                          |
|------------------------------------------------------------------------------------------------------|----------------------------------|
| <span id="0"></span><dl> <dt>**0**</dt> </dl> | Il report non è supportato.<br/> |
| <span id="1"></span><dl> <dt>**1**</dt> </dl> | Errore.<br/>                |
| <span id="2"></span><dl> <dt>**2**</dt> </dl> | Accesso negato.<br/>        |
| <span id="3"></span><dl> <dt>**3**</dt> </dl> | Inizializzazione.<br/>         |
| <span id="4"></span><dl> <dt>**4**</dt> </dl> | In esecuzione.<br/>              |



 

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Questo evento non restituisce un valore.

## <a name="remarks"></a>Commenti

È necessario implementare gestori di report di modifica dello stato distinti per i report degli indirizzi civici e i report di Latitudine/Longitudine.

## <a name="examples"></a>Esempio

Per un esempio di come usare questo evento, vedere [ascolto degli eventi del report LatLong](/uwp/api/Windows.Devices.Geolocation).

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|--------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows 7\]<br/> |
| Server minimo supportato<br/> | Nessuno supportato<br/>                  |



 

