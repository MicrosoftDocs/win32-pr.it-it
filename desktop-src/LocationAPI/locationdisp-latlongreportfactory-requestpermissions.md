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
ms.openlocfilehash: ffbae03d22cee89b5974b32b224c779210e82feb23292628a5a705bc203dbc5e
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120129831"
---
# <a name="locationdisplatlongreportfactoryrequestpermissions-method"></a>Metodo LocationDisp.LatLongReportFactory.RequestPermissions

\[Il modello a oggetti dell'API Location è disponibile per l'uso nei sistemi operativi specificati nella sezione Requisiti. È possibile che in versioni successive sia stata modificata o non sia più disponibile. Per accedere invece alla posizione da un sito Web, usare [l'API di georilevazione W3C](/previous-versions/windows/internet-explorer/ie-developer/samples/gg589513(v=vs.85)). Per accedere alla posizione da un'applicazione desktop, usare il [**Windows. API Devices.Geolocation.**](/uwp/api/Windows.Devices.Geolocation)\]

Apre una finestra di dialogo di sistema per richiedere l'autorizzazione utente per i dispositivi abilitati per la posizione.

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
> Se un'applicazione in esecuzione in modalità protetta, ad esempio un oggetto browser helper (BHO) per Internet Explorer, chiama **RequestPermissions** e **l'utente sceglie l'opzione** Non abilitare questo sensore di posizione nella finestra di dialogo, il provider di posizione non verrà abilitato, ma Windows visualizza nuovamente la finestra di dialogo se **RequestPermissions** viene chiamato di nuovo dallo stesso utente. Le applicazioni in esecuzione in modalità protetta possono scegliere di non chiamare **RequestPermissions** all'avvio in modo che l'utente non veda una finestra di dialogo potenzialmente indesiderata ogni volta che l'applicazione viene avviata.

 

## <a name="examples"></a>Esempio

Per un esempio di come usare questo metodo, vedere Ascolto di eventi del [report LatLong](/uwp/api/Windows.Devices.Geolocation).

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|--------------------------------------------|
| Client minimo supportato<br/> | Windows 7 \[ app desktop\]<br/> |
| Server minimo supportato<br/> | Nessuno supportato<br/>                  |



 

