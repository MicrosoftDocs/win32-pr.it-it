---
description: Apre una finestra di dialogo di sistema per richiedere l'autorizzazione utente per i dispositivi abilitati per la posizione.
ms.assetid: b213591a-2830-4979-b532-e71cdef1b994
title: LocationDisp. CivicAddressReportFactory. RequestPermissions, metodo
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- LocationDisp.CivicAddressReportFactory.RequestPermissions
api_type:
- COM
api_location: ''
ms.openlocfilehash: 6d027687302c544974d13b1ba50194e8d6003a94
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104349776"
---
# <a name="locationdispcivicaddressreportfactoryrequestpermissions-method"></a>LocationDisp. CivicAddressReportFactory. RequestPermissions, metodo

\[Il modello a oggetti dell'API location è disponibile per l'uso nei sistemi operativi specificati nella sezione requisiti. È possibile che in versioni successive sia stata modificata o non sia più disponibile. Per accedere al percorso da un sito Web, usare invece l' [API di georilevazione W3C](/previous-versions/windows/internet-explorer/ie-developer/samples/gg589513(v=vs.85)). Per accedere alla posizione da un'applicazione desktop, usare l'API [**Windows. Devices. Geolocation**](/uwp/api/Windows.Devices.Geolocation) .\]

Apre una finestra di dialogo di sistema per richiedere l'autorizzazione utente per i dispositivi abilitati per la posizione.

## <a name="syntax"></a>Sintassi


```JScript
LocationDisp.CivicAddressReportFactory.RequestPermissions(
  hWnd
)
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*hWnd* 
</dt> <dd>

Questo parametro non viene utilizzato e deve essere impostato su zero.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Questo metodo non restituisce valori.

## <a name="remarks"></a>Commenti

La chiamata è sincrona e il chiamante attende la chiusura della finestra di dialogo.

> [!Note]  
> Se un'applicazione in esecuzione in modalità protetta, ad esempio un oggetto browser helper (BHO) per Internet Explorer, chiama **RequestPermissions** e l'utente sceglie l'opzione **non abilitare il sensore della posizione** nella finestra di dialogo, il provider di percorsi non verrà abilitato, ma Windows visualizzerà nuovamente la finestra di dialogo se **RequestPermissions** viene chiamato nuovamente dallo stesso utente. Le applicazioni in esecuzione in modalità protetta possono scegliere di non chiamare [**RequestPermissions**](/windows/win32/api/locationapi/nf-locationapi-ilocation-requestpermissions) all'avvio in modo che l'utente non visualizzi una finestra di dialogo probabilmente indesiderata ogni volta che l'applicazione viene avviata.

 

## <a name="examples"></a>Esempio

Per un esempio di come usare questo metodo, vedere [ascolto di eventi di report di indirizzi civici](/uwp/api/Windows.Devices.Geolocation).

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|--------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows 7\]<br/> |
| Server minimo supportato<br/> | Nessuno supportato<br/>                  |



 

