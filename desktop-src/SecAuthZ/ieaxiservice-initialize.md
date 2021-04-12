---
description: Verifica e Scarica un oggetto ActiveX.
ms.assetid: a477c6dc-32a7-4d17-a997-6df4967d6c55
title: 'Metodo IeAxiService:: Initialize'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IeAxiService.Initialize
api_type:
- COM
api_location: ''
ms.openlocfilehash: 2b2e388f955c968220223519150fc4dc5b7af4a6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104233694"
---
# <a name="ieaxiserviceinitialize-method"></a>Metodo IeAxiService:: Initialize

Il metodo **Initialize** controlla e Scarica un oggetto ActiveX. Se l'oggetto soddisfa i requisiti dei criteri, questo metodo inizializza un oggetto di sistema che installa l'oggetto ActiveX.

## <a name="syntax"></a>Sintassi


```C++
SECURITY_STATUS Initialize(
  [in]  HWND     hwndParent,
  [in]  DWORD    dwClientPID,
  [in]  BSTR     bstrDesktop,
  [in]  BSTR     bstrClsID,
  [in]  BSTR     bstrURL,
  [out] BSTR     *pbstrNonce,
  [out] IUnknown **ppISyncBrokerInterface
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*hwndParent* \[ in\]
</dt> <dd>

Handle per la finestra padre della finestra che tenta di installare il controllo ActiveX.

</dd> <dt>

*dwClientPID* \[ in\]
</dt> <dd>

ID processo del processo chiamante.

</dd> <dt>

*bstrDesktop* \[ in\]
</dt> <dd>

Desktop per l'oggetto.

</dd> <dt>

*bstrClsID* \[ in\]
</dt> <dd>

ID classe dell'oggetto ActiveX da installare.

</dd> <dt>

*bstrURL* \[ in\]
</dt> <dd>

URL dell'oggetto ActiveX da installare.

</dd> <dt>

*pbstrNonce* \[ out\]
</dt> <dd>

Contesto che può essere utilizzato per condividere le informazioni sullo stato nelle chiamate ad altri metodi utilizzati per verificare e scaricare l'oggetto ActiveX.

</dd> <dt>

*ppISyncBrokerInterface* \[ out\]
</dt> <dd>

Puntatore all'istanza dell'interfaccia [**IeAxiSystemInstaller**](ieaxisysteminstaller.md) che installa il controllo ActiveX.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Se la funzione ha esito positivo, il valore restituito è \_ OK.

Se la funzione ha esito negativo, il valore restituito può essere uno dei seguenti codici di errore.



| Codice/valore restituito                                                                                                                                                              | Descrizione                                            |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------|
| <dl> <dt>**Attendibilità \_ E \_ soggetto \_ non \_ attendibile**</dt> <dt>0x800B0004</dt> </dl> | L'oggetto ActiveX non deve essere installato.<br/> |



 

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Vista Business, Windows Vista Enterprise, Windows Vista Ultimate \[ desktop apps\]<br/> |
| Server minimo supportato<br/> | Nessuno supportato<br/>                                                                                 |
| IID<br/>                      | IID \_ IeAxiService è definito come E9E92380-9ECD-4982-A0EB-6815A56CCF27<br/>                           |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**IeAxiService**](ieaxiservice.md)
</dt> </dl>

 

 




