---
title: Metodo IBackgroundCopyFile2 seremotename (Deliveryoptimization. h)
description: Consente di modificare il nome remoto in un nuovo URL in un processo di download.
ms.assetid: 344D4193-C96E-4B94-AA53-F9307FEB2565
keywords:
- Seremotename (metodo)
- Metodo seremotename, interfaccia IBackgroundCopyFile2
- Interfaccia IBackgroundCopyFile2, metodo seremotename
topic_type:
- apiref
api_name:
- IBackgroundCopyFile2.SetRemoteName
api_location:
- dosvc.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 4afb5448144867c799bd401bc2d7c180d3958f2a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104476366"
---
# <a name="ibackgroundcopyfile2setremotename-method"></a>Metodo IBackgroundCopyFile2:: seremotename

Consente di modificare il nome remoto in un nuovo URL in un processo di download.

## <a name="syntax"></a>Sintassi


```C++
HRESULT SetRemoteName(
  [in] LPCWSTR RemoteName
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*RemoteName* \[ in\]
</dt> <dd>

Stringa con terminazione null che contiene il nome del file nel server. Per informazioni su come specificare il nome remoto, vedere il membro **RemoteName** .

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Questo metodo restituisce i valori restituiti seguenti e altri.



| Codice restituito                                                                                  | Descrizione                                                                                                           |
|----------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>S_OK * * * *</dt> </dl>     | Operazione riuscita<br/>                                                                                                    |
| <dl> <dt>**E_INVALIDARG**</dt> </dl> | Il nuovo nome remoto è un URL non valido o il nuovo URL è troppo lungo (l'URL non può superare i 2.200 caratteri).<br/> |



 

## <a name="remarks"></a>Commenti

In genere, questo metodo viene chiamato se si vuole modificare l'URL usato per trasferire il file o se si vuole modificare il nome o il percorso del file.

Questo metodo non serializza quando restituisce. Per serializzare la modifica, [**sospendere**](ibackgroundcopyjob-suspend.md) il processo, chiamare questo metodo (se si modificano più file nel processo, usare un ciclo) e [**riprendere**](ibackgroundcopyjob-resume.md) il processo. La chiamata al metodo **Metodo ibackgroundcopyjob:: Resume** serializza la modifica.

Se il timestamp o le dimensioni del file del nuovo nome remoto sono diverse dal nome remoto precedente o se il nuovo server non supporta il ripristino del checkpoint (per i nomi remoti HTTP), riavviare il download. In caso contrario, il trasferimento riprende dalla stessa posizione nel nuovo server. DO non riavvia i file già trasferiti.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-----------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Solo app desktop Windows 10 versione 1709 \[\]<br/>                                           |
| Server minimo supportato<br/> | Windows Server, versione 1709 \[ solo per le app desktop\]<br/>                                       |
| Intestazione<br/>                   | <dl> <dt>Deliveryoptimization. h</dt> </dl>   |
| IDL<br/>                      | <dl> <dt>DeliveryOptimization. idl</dt> </dl> |
| Libreria<br/>                  | <dl> <dt>Dosvc. lib</dt> </dl>                |
| DLL<br/>                      | <dl> <dt>Dosvc.dll</dt> </dl>                |
| IID<br/>                      | IID_IBackgroundCopyFile2 viene definito come 83e81b93-0873-474d-8A8C-f2018b1a939c<br/>             |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**IBackgroundCopyFile2**](ibackgroundcopyfile2.md)
</dt> </dl>

 

 





