---
title: Metodo INapComponentConfig2 InvokeUIFromConfigBlob (NapCommon.h)
description: Viene implementato dai validator di integrità del sistema (SHV) in base alle esigenze per caricare la configurazione di un computer remoto o locale in memoria e visualizzare un'interfaccia utente che consente la manipolazione dei dati di configurazione.
ms.assetid: 9c012690-6751-4a47-8683-74abac610c77
keywords:
- Metodo InvokeUIFromConfigBlob NAP
- Metodo InvokeUIFromConfigBlob NAP, interfaccia INapComponentConfig2
- Interfaccia INapComponentConfig2 NAP, metodo InvokeUIFromConfigBlob
topic_type:
- apiref
api_name:
- INapComponentConfig2.InvokeUIFromConfigBlob
api_location:
- NapCommon.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 45d85e0506b8adf084b65a13a117a9dea3856fcff2e73f65a229bdb31b283fb9
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119803161"
---
# <a name="inapcomponentconfig2invokeuifromconfigblob-method"></a>Metodo INapComponentConfig2::InvokeUIFromConfigBlob

> [!Note]  
> La piattaforma Protezione accesso alla rete non è disponibile a partire da Windows 10

 

Il **metodo InvokeUIFromConfigBlob** viene implementato dai validator di integrità del sistema (SHV) in base alle esigenze per caricare la configurazione di un computer remoto o locale in memoria e visualizzare un'interfaccia utente che consente la manipolazione dei dati di configurazione. Il componente di configurazione deve supportare l'utilizzo [**di INapComponentConfig**](inapcomponentconfig.md) tramite DCOM.

## <a name="syntax"></a>Sintassi


```C++
HRESULT InvokeUIFromConfigBlob(
  [in, unique] HWND   hwndParent,
  [in]         UINT16 inbCount,
  [in]         BYTE   *inData,
  [out]        UINT16 *outbCount,
  [out]        BYTE   **outdata,
  [out]        BOOL   *fConfigChanged
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*hwndParent* \[ Pollici\]
</dt> <dd>

Handle per la finestra padre o proprietaria. È necessario specificare un handle di finestra valido.

</dd> <dt>

*inbCount* \[ Pollici\]
</dt> <dd>

Dimensioni, in byte, di *inData.*

</dd> <dt>

*inData* \[ Pollici\]
</dt> <dd>

Puntatore a un buffer in cui sono archiviati i dati di configurazione iniziali. Questi dati vengono esportati dal computer remoto o locale.

</dd> <dt>

*outbCount* \[ Cambio\]
</dt> <dd>

Dimensione, in byte, di *outdata.*

</dd> <dt>

*outdata* \[ Cambio\]
</dt> <dd>

Puntatore a un buffer che archivia i dati di configurazione modificati dall'interfaccia utente di configurazione SHV. Questi dati vengono importati dal computer remoto o locale.

</dd> <dt>

*fConfigChanged* \[ Cambio\]
</dt> <dd>

Puntatore a un **oggetto BOOL impostato** su **TRUE se** la configurazione è stata modificata durante l'operazione dell'interfaccia utente e FALSE in **caso contrario.**

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce S \_ OK in caso di esito positivo o uno dei codici di Windows standard.

## <a name="remarks"></a>Commenti

Se usata per un computer locale, questa funzione può essere usata per la configurazione SHV dei criteri. Fornisce un modo per richiamare un'interfaccia utente SHV e modificare una configurazione SHV esistente.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Nessuno supportato<br/>                                                                |
| Server minimo supportato<br/> | Windows Solo app desktop di Server 2008 \[\]<br/>                                     |
| Intestazione<br/>                   | <dl> <dt>NapCommon.h</dt> </dl>   |
| Idl<br/>                      | <dl> <dt>NapCommon.idl</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**INapComponentConfig2**](inapcomponentconfig2.md)
</dt> </dl>

 

 





