---
description: "Metodo LocationDisp.CivicAddressReportFactory.RequestPermissions: apre una finestra di dialogo di sistema per richiedere l'autorizzazione utente per i dispositivi abilitati per la posizione."
ms.assetid: b213591a-2830-4979-b532-e71cdef1b994
title: Metodo LocationDisp.CivicAddressReportFactory.RequestPermissions
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
ms.openlocfilehash: cab163585fa23839eb894f7ad83f29ed7975e589
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/28/2021
ms.locfileid: "108110909"
---
# <a name="locationdispcivicaddressreportfactoryrequestpermissions-method"></a>Metodo LocationDisp.CivicAddressReportFactory.RequestPermissions

\[Il modello a oggetti dell'API Location è disponibile per l'uso nei sistemi operativi specificati nella sezione Requisiti. È possibile che in versioni successive sia stata modificata o non sia più disponibile. Per accedere invece alla posizione da un sito Web, usare [l'API di georilevazione W3C](/previous-versions/windows/internet-explorer/ie-developer/samples/gg589513(v=vs.85)). Per accedere alla posizione da un'applicazione desktop, usare l'API [**Windows.Devices.Geolocation.**](/uwp/api/Windows.Devices.Geolocation)\]

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

Questo parametro non viene usato e deve essere impostato su zero.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Questo metodo non restituisce valori.

## <a name="remarks"></a>Commenti

La chiamata è sincrona e il chiamante attende la chiusura della finestra di dialogo.

> [!Note]  
> Se un'applicazione in esecuzione in modalità protetta, ad esempio un oggetto browser helper (BHO) per Internet Explorer, chiama **RequestPermissions** e **l'utente sceglie l'opzione** Non abilitare questo sensore di posizione nella finestra di dialogo, il provider di percorso non verrà abilitato, ma Windows visualizza di nuovo la finestra di dialogo se **RequestPermissions** viene chiamato di nuovo dallo stesso utente. Le applicazioni in esecuzione in modalità protetta possono scegliere di non chiamare [**RequestPermissions**](/windows/win32/api/locationapi/nf-locationapi-ilocation-requestpermissions) all'avvio in modo che l'utente non veda una finestra di dialogo potenzialmente indesiderata ogni volta che l'applicazione viene avviata.

 

## <a name="examples"></a>Esempio

Per un esempio di come usare questo metodo, vedere [Listening for Civic Address Report Events](/uwp/api/Windows.Devices.Geolocation).

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|--------------------------------------------|
| Client minimo supportato<br/> | Solo app desktop di Windows 7 \[\]<br/> |
| Server minimo supportato<br/> | Nessuno supportato<br/>                  |



 

