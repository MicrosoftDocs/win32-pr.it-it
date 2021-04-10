---
title: Metodo GetIcon INapComponentInfo (NapCommon. h)
description: Viene utilizzato dal sistema NAP per ottenere l'icona di un client di integrità.
ms.assetid: 6501fe12-1ec0-43a1-b672-b6cfd9a08d85
keywords:
- Metodo GetIcon (NAP)
- Metodo GetIcon, NAP, interfaccia INapComponentInfo
- Interfaccia INapComponentInfo NAP, Metodo GetIcon
topic_type:
- apiref
api_name:
- INapComponentInfo.GetIcon
api_location:
- NapCommon.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 795ad85f8497262f88fa55d8efb2da7466b8c3a9
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103964835"
---
# <a name="inapcomponentinfogeticon-method"></a>Metodo INapComponentInfo:: GetIcon

> [!Note]  
> La piattaforma protezione accesso alla rete non è disponibile a partire da Windows 10

 

Il metodo di callback **INapComponentInfo:: GetIcon** viene utilizzato dal sistema NAP per ottenere l'icona di un client di integrità.

## <a name="syntax"></a>Sintassi


```C++
HRESULT GetIcon(
  [out] CountedString **dllFilePath,
  [out] UINT32        *iconResourceId
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*dllFilePath* \[ out\]
</dt> <dd>

Puntatore a un puntatore a un [**CountedString**](/windows/win32/api/naptypes/ns-naptypes-countedstring) utilizzato per restituire il percorso del file dll che contiene l'icona.

</dd> <dt>

*iconResourceId* \[ out\]
</dt> <dd>

Puntatore al valore usato per restituire l'ID risorsa dell'icona da usare.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce uno di questi codici di errore in base al risultato di questa operazione.



| Codice restituito                                                                                     | Descrizione                                                        |
|-------------------------------------------------------------------------------------------------|--------------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>           | L'operazione è riuscita.<br/>                            |
| <dl> <dt>**E \_ ACCESSDENIED**</dt> </dl> | Errore delle autorizzazioni, accesso negato.<br/>                       |
| <dl> <dt>**E \_ OUTOFMEMORY**</dt> </dl>  | Limite di risorse di sistema. Impossibile eseguire l'operazione.<br/> |



 

## <a name="remarks"></a>Commenti

Le icone devono essere localizzate in base all'ID lingua del thread chiamante.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows Vista\]<br/>                                           |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2008\]<br/>                                     |
| Intestazione<br/>                   | <dl> <dt>NapCommon. h</dt> </dl>   |
| IDL<br/>                      | <dl> <dt>NapCommon. idl</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>


</dt> <dt>

[**INapComponentInfo**](inapcomponentinfo.md)
</dt> </dl>

 

 





