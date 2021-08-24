---
title: Metodo IBackgroundCopyFile2 SetRemoteName (Deliveryoptimization.h)
description: Modifica il nome remoto in un nuovo URL in un processo di download.
ms.assetid: 344D4193-C96E-4B94-AA53-F9307FEB2565
keywords:
- Metodo SetRemoteName
- Metodo SetRemoteName, interfaccia IBackgroundCopyFile2
- Interfaccia IBackgroundCopyFile2, metodo SetRemoteName
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
ms.openlocfilehash: e4a2ed93a264aa12d61291c3562a455a026e0dfd0d727648b7d13f6ffe360015
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119636021"
---
# <a name="ibackgroundcopyfile2setremotename-method"></a>Metodo IBackgroundCopyFile2::SetRemoteName

Modifica il nome remoto in un nuovo URL in un processo di download.

## <a name="syntax"></a>Sintassi


```C++
HRESULT SetRemoteName(
  [in] LPCWSTR RemoteName
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*RemoteName* \[ Pollici\]
</dt> <dd>

Stringa con terminazione Null che contiene il nome del file nel server. Per informazioni su come specificare il nome remoto, vedere il **membro RemoteName.**

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Questo metodo restituisce i valori restituiti seguenti, oltre ad altri.



| Codice restituito                                                                                  | Descrizione                                                                                                           |
|----------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>S_OK****</dt> </dl>     | Operazione riuscita<br/>                                                                                                    |
| <dl> <dt>**E_INVALIDARG**</dt> </dl> | Il nuovo nome remoto è un URL non valido o il nuovo URL è troppo lungo (l'URL non può superare i 2.200 caratteri).<br/> |



 

## <a name="remarks"></a>Commenti

In genere, questo metodo viene chiamato se si vuole modificare l'URL usato per trasferire il file o se si vuole modificare il nome o il percorso del file.

Questo metodo non esegue la serializzazione quando viene restituito. Per serializzare la modifica, [**sospendere**](ibackgroundcopyjob-suspend.md) il processo, chiamare questo metodo (se si modificano più file nel processo, usare un ciclo) e [**riprendere**](ibackgroundcopyjob-resume.md) il processo. La chiamata **al metodo IBackgroundCopyJob::Resume** serializza la modifica.

Se il timestamp o le dimensioni del file del nuovo nome remoto sono diverse dal nome remoto precedente o se il nuovo server non supporta la ripresa del checkpoint (per i nomi remoti HTTP), DO riavvia il download. In caso contrario, il trasferimento riprende dalla stessa posizione nel nuovo server. DO non riavvia i file già trasferiti.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-----------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 10, solo app desktop versione 1709 \[\]<br/>                                           |
| Server minimo supportato<br/> | Windows Server, solo app desktop versione 1709 \[\]<br/>                                       |
| Intestazione<br/>                   | <dl> <dt>Deliveryoptimization.h</dt> </dl>   |
| Idl<br/>                      | <dl> <dt>DeliveryOptimization.idl</dt> </dl> |
| Libreria<br/>                  | <dl> <dt>Dosvc.lib</dt> </dl>                |
| DLL<br/>                      | <dl> <dt>Dosvc.dll</dt> </dl>                |
| IID<br/>                      | IID_IBackgroundCopyFile2 è definito come 83e81b93-0873-474d-8a8c-f2018b1a939c<br/>             |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**IBackgroundCopyFile2**](ibackgroundcopyfile2.md)
</dt> </dl>

 

 





