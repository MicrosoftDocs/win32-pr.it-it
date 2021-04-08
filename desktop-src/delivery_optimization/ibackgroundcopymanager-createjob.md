---
title: Metodo IBackgroundCopyManager CreateJob (Deliveryoptimization. h)
description: Crea un processo.
ms.assetid: BDE5BE4D-9AE9-463D-B900-850D255EAB58
keywords:
- Metodo CreateJob
- Metodo CreateJob, interfaccia IBackgroundCopyManager
- Interfaccia IBackgroundCopyManager, metodo CreateJob
topic_type:
- apiref
api_name:
- IBackgroundCopyManager.CreateJob
api_location:
- dosvc.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: de7f0b61cdbc5d5776039c3bf13b83ca0a6f8fdc
ms.sourcegitcommit: ea73413ee4f69fa573ee0cd4422f20d17bd42e1f
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/27/2021
ms.locfileid: "104058393"
---
# <a name="ibackgroundcopymanagercreatejob-method"></a>Metodo IBackgroundCopyManager:: CreateJob

Crea un processo.

## <a name="syntax"></a>Sintassi


```C++
HRESULT CreateJob(
  [in]  LPCWSTR            pDisplayName,
  [in]  BG_JOB_TYPE        Type,
  [out] GUID               *pJobID,
  [out] IBackgroundCopyJob **ppJob
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*pDisplayName* \[ in\]
</dt> <dd>

Stringa con terminazione null che contiene un nome visualizzato per il processo. In genere, il nome visualizzato viene usato per identificare il processo in un'interfaccia utente. Si noti che più processi possono avere lo stesso nome visualizzato. Non può essere **null**. Il nome è limitato a 256 caratteri, escluso il carattere di terminazione null.

</dd> <dt>

*Tipo* \[ di in\]
</dt> <dd>

Tipo di processo di trasferimento, ad esempio BG_JOB_TYPE_DOWNLOAD. Per un elenco dei tipi di trasferimento, vedere l'enumerazione [**BG_JOB_TYPE**](bg-job-type.md) .

</dd> <dt>

*pJobID* \[ out\]
</dt> <dd>

Identifica in modo univoco il processo nella coda. Usare questo identificatore quando si chiama il metodo [**IBackgroundCopyManager:: GetJob**](ibackgroundcopymanager-getjob.md) per ottenere un processo dalla coda.

</dd> <dt>

*ppJob* \[ out\]
</dt> <dd>

Puntatore a interfaccia [**Metodo ibackgroundcopyjob**](ibackgroundcopyjob-.md) che consente di modificare le proprietà del processo e di specificare i file da trasferire. Per attivare il processo nella coda, chiamare il metodo [**Metodo ibackgroundcopyjob:: Resume**](ibackgroundcopyjob-resume.md) . Rilasciare *ppJob* al termine.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Questo metodo restituisce i valori **HRESULT** seguenti e altri.



| Codice restituito                                                                              | Descrizione                                    |
|------------------------------------------------------------------------------------------|------------------------------------------------|
| <dl> <dt>S_OK * * * *</dt> </dl> | Generazione del nuovo processo completata.<br/> |



 

## <a name="remarks"></a>Commenti

Solo l'utente che crea il processo o un utente con privilegi di amministratore può [aggiungere file al processo](https://www.bing.com/search?q=add+files+to+the+job) e [modificare le proprietà del processo](https://www.bing.com/search?q=change+the+job's+properties).

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-----------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Solo app desktop Windows 10 versione 1709 \[\]<br/>                                           |
| Server minimo supportato<br/> | Windows Server, versione 1709 \[ solo per le app desktop\]<br/>                                       |
| Intestazione<br/>                   | <dl> <dt>Deliveryoptimization. h</dt> </dl>   |
| IDL<br/>                      | <dl> <dt>DeliveryOptimization. idl</dt> </dl> |
| Libreria<br/>                  | <dl> <dt>Dosvc. lib</dt> </dl>                |
| DLL<br/>                      | <dl> <dt>Dosvc.dll</dt> </dl>                |
| IID<br/>                      | IID_IBackgroundCopyManager viene definito come 5CE34C0D-0DC9-4C1F-897C-DAA1B78CEE7C<br/>           |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**IBackgroundCopyManager**](ibackgroundcopymanager.md)
</dt> <dt>

[**Metodo ibackgroundcopyjob**](ibackgroundcopyjob-.md)
</dt> <dt>

[**Metodo ibackgroundcopyjob:: Resume**](ibackgroundcopyjob-resume.md)
</dt> </dl>
