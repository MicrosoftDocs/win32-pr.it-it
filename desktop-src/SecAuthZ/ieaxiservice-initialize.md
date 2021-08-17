---
description: Controlla e scarica un oggetto ActiveX corrente.
ms.assetid: a477c6dc-32a7-4d17-a997-6df4967d6c55
title: Metodo IeAxiService::Initialize
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
ms.openlocfilehash: 911d955f84d81b225a1b4062e47b2b9b6ab6d058aa6df2e6a72a8d40242345a2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119414891"
---
# <a name="ieaxiserviceinitialize-method"></a>Metodo IeAxiService::Initialize

Il **metodo Initialize** controlla e scarica un ActiveX oggetto . Se l'oggetto soddisfa i requisiti dei criteri, questo metodo inizializza un oggetto di sistema che installa l ActiveX o object.

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

*hwndParent* \[ Pollici\]
</dt> <dd>

Handle per la finestra padre della finestra che sta tentando di installare il controllo ActiveX controllo .

</dd> <dt>

*dwClientPID* \[ Pollici\]
</dt> <dd>

ID del processo chiamante.

</dd> <dt>

*bstrDesktop* \[ Pollici\]
</dt> <dd>

Desktop per l'oggetto .

</dd> <dt>

*bstrClsID* \[ Pollici\]
</dt> <dd>

ID di classe dell'ActiveX da installare.

</dd> <dt>

*bstrURL* \[ Pollici\]
</dt> <dd>

URL dell'oggetto ActiveX da installare.

</dd> <dt>

*pbstrNonce* \[ Cambio\]
</dt> <dd>

Contesto che può essere usato per condividere le informazioni sullo stato nelle chiamate ad altri metodi usati per verificare e scaricare l'ActiveX corrente.

</dd> <dt>

*ppISyncBrokerInterface* \[ Cambio\]
</dt> <dd>

Puntatore all'istanza [**dell'interfaccia IeAxiSystemInstaller**](ieaxisysteminstaller.md) che installa il ActiveX controllo.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Se la funzione ha esito positivo, il valore restituito è S \_ OK.

Se la funzione ha esito negativo, il valore restituito può essere uno dei codici di errore seguenti.



| Codice/valore restituito                                                                                                                                                              | Descrizione                                            |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------|
| <dl> <dt>**TRUST \_ E \_ SUBJECT NOT TRUSTED \_ \_ 0x800B0004**</dt> <dt></dt> </dl> | L ActiveX o object non deve essere installato.<br/> |



 

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Vista Business, Windows Vista Enterprise, Windows solo app desktop di Vista Ultimate \[\]<br/> |
| Server minimo supportato<br/> | Nessuno supportato<br/>                                                                                 |
| IID<br/>                      | IeAxiService IID è definito come \_ E9E92380-9ECD-4982-A0EB-6815A56CCF27<br/>                           |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**IeAxiService**](ieaxiservice.md)
</dt> </dl>

 

 




