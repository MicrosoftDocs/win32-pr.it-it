---
description: Consente di visualizzare un'interfaccia utente selezionabile che consente di selezionare un nome utente.
ms.assetid: 0a02d9e5-b2cf-4818-a2e1-89e6019e53d4
title: 'Metodo ISCrdEnr:: selectUserName'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISCrdEnr.selectUserName
- SCrdEnr.selectUserName
api_type:
- COM
api_location:
- Scrdenrl.dll
ms.openlocfilehash: 13059775abc8520c39a0ad3dea2d604fc8d65455
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106316661"
---
# <a name="iscrdenrselectusername-method"></a>Metodo ISCrdEnr:: selectUserName

Il metodo **selectUserName** Visualizza un'interfaccia **utente SELECT** , consentendo la selezione di un nome utente.

Il nome utente viene applicato all'utente per conto del quale è destinata la registrazione del certificato.

## <a name="syntax"></a>Sintassi


```C++
HRESULT selectUserName(
  [in] DWORD dwFlags
);
```


```VB

SCrdEnr.selectUserName( _
  ByVal dwFlags _
)
```





## <a name="parameters"></a>Parametri

<dl> <dt>

*dwFlags* \[ in\]
</dt> <dd>

Riservato per utilizzi futuri. Impostare questo valore su zero.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

### <a name="vb"></a>VB

Se il metodo ha esito positivo, il metodo restituisce S \_ OK.

Se il metodo ha esito negativo, restituisce un valore **HRESULT** che indica l'errore. Per un elenco di codici di errore comuni, vedere [valori HRESULT comuni](common-hresult-values.md).

## <a name="remarks"></a>Commenti

Utilizzare questo metodo per selezionare il nome dell'utente. Dopo aver selezionato un nome utente, è possibile recuperarne il valore chiamando il metodo [**ISCrdEnr:: GetUserName**](iscrdenr-getusername.md) .

Un'alternativa all'uso dell'interfaccia ' Seleziona utente ' consiste nel specificare un utente chiamando il metodo [**ISCrdEnr:: Seusername**](iscrdenr-setusername.md) .

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Nessuno supportato<br/>                                                               |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2003\]<br/>                                    |
| DLL<br/>                      | <dl> <dt>Scrdenrl.dll</dt> </dl> |
| IID<br/>                      | IID \_ ISCrdEnr è definito come 753988a1-1357-436D-9cf5-f089bdd67d64<br/>             |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**ISCrdEnr**](iscrdenr.md)
</dt> <dt>

[**ISCrdEnr:: GetUserName**](iscrdenr-getusername.md)
</dt> <dt>

[**ISCrdEnr::resetUser**](iscrdenr-resetuser.md)
</dt> <dt>

[**ISCrdEnr:: seusername**](iscrdenr-setusername.md)
</dt> </dl>

 

 




