---
description: "Metodo LocationDisp.LatLongReportFactory.RequestPermissions: apre una finestra di dialogo di sistema per richiedere l'autorizzazione utente per i dispositivi abilitati per la posizione."
ms.assetid: 25b4368d-ff9d-4806-a22e-4ae0760d6f0f
title: Metodo LocationDisp.LatLongReportFactory.RequestPermissions
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- LocationDisp.LatLongReportFactory.RequestPermissions
api_type:
- COM
api_location: ''
ms.openlocfilehash: 1b2d21a032a2e4c08c6f80e4f0ae79349a49ce21
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/28/2021
ms.locfileid: "108088929"
---
# <a name="locationdisplatlongreportfactoryrequestpermissions-method"></a>Metodo LocationDisp.LatLongReportFactory.RequestPermissions

\[Il modello a oggetti dell'API Location è disponibile per l'uso nei sistemi operativi specificati nella sezione Requisiti. È possibile che in versioni successive sia stata modificata o non sia più disponibile. Per accedere invece alla posizione da un sito Web, usare [l'API di georilevazione W3C](/previous-versions/windows/internet-explorer/ie-developer/samples/gg589513(v=vs.85)). Per accedere alla posizione da un'applicazione desktop, usare l'API [**Windows.Devices.Geolocation.**](/uwp/api/Windows.Devices.Geolocation)\]

Apre una finestra di dialogo di sistema per richiedere l'autorizzazione utente per i dispositivi abilitati alla posizione.

## <a name="syntax"></a>Sintassi


```JScript
LocationDisp.LatLongReportFactory.RequestPermissions(
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
> Se un'applicazione in esecuzione in modalità protetta, ad esempio un oggetto browser helper per Internet Explorer, chiama **RequestPermissions** e **l'utente sceglie l'opzione** Non abilitare questo sensore di posizione nella finestra di dialogo, il provider di posizione non verrà abilitato, ma Windows visualizza di nuovo la finestra di dialogo se **RequestPermissions** viene chiamato di nuovo dallo stesso utente. Le applicazioni eseguite in modalità protetta possono scegliere di non chiamare **RequestPermissions** all'avvio, in modo che l'utente non veda una finestra di dialogo potenzialmente indesiderata a ogni avvio dell'applicazione.

 

## <a name="examples"></a>Esempio

Per un esempio di come usare questo metodo, vedere [Listening for LatLong Report Events](/uwp/api/Windows.Devices.Geolocation).

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|--------------------------------------------|
| Client minimo supportato<br/> | Solo app desktop di Windows 7 \[\]<br/> |
| Server minimo supportato<br/> | Nessuno supportato<br/>                  |



 

