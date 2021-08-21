---
title: Metodo INapComponentInfo GetIcon (NapCommon.h)
description: Viene utilizzato dal sistema di Protezione accesso alla rete per ottenere l'icona di un client di integrità.
ms.assetid: 6501fe12-1ec0-43a1-b672-b6cfd9a08d85
keywords:
- Metodo GetIcon NAP
- Metodo GetIcon NAP, interfaccia INapComponentInfo
- Interfaccia INapComponentInfo NAP, metodo GetIcon
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
ms.openlocfilehash: 1711c186d107418d95ccaf19e2a1440b0cecfc0e32fc8c425754d2d9fc19a9d6
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118134435"
---
# <a name="inapcomponentinfogeticon-method"></a>Metodo INapComponentInfo::GetIcon

> [!Note]  
> La piattaforma Protezione accesso alla rete non è disponibile a partire da Windows 10

 

Il metodo di callback **INapComponentInfo::GetIcon** viene usato dal sistema nap per ottenere l'icona di un client di integrità.

## <a name="syntax"></a>Sintassi


```C++
HRESULT GetIcon(
  [out] CountedString **dllFilePath,
  [out] UINT32        *iconResourceId
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*dllFilePath* \[ Cambio\]
</dt> <dd>

Puntatore a un puntatore a [**un oggetto CountedString utilizzato**](/windows/win32/api/naptypes/ns-naptypes-countedstring) per restituire il percorso del file della DLL che contiene l'icona.

</dd> <dt>

*iconResourceId* \[ Cambio\]
</dt> <dd>

Puntatore al valore usato per restituire l'ID risorsa dell'icona da usare.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce uno di questi codici di errore in base al risultato di questa operazione.



| Codice restituito                                                                                     | Descrizione                                                        |
|-------------------------------------------------------------------------------------------------|--------------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>           | L'operazione è riuscita.<br/>                            |
| <dl> <dt>**E \_ ACCESSO NEGATO**</dt> </dl> | Errore di autorizzazione, accesso negato.<br/>                       |
| <dl> <dt>**E \_ OUTOFMEMORY**</dt> </dl>  | Limite di risorse di sistema. Impossibile eseguire l'operazione.<br/> |



 

## <a name="remarks"></a>Commenti

Le icone devono essere localizzate in base all'ID lingua del thread chiamante.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo \[ app desktop Vista\]<br/>                                           |
| Server minimo supportato<br/> | Windows Solo app desktop di Server 2008 \[\]<br/>                                     |
| Intestazione<br/>                   | <dl> <dt>NapCommon.h</dt> </dl>   |
| Idl<br/>                      | <dl> <dt>NapCommon.idl</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>


</dt> <dt>

[**INapComponentInfo**](inapcomponentinfo.md)
</dt> </dl>

 

 





