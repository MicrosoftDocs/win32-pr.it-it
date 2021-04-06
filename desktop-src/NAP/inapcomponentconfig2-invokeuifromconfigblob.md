---
title: Metodo INapComponentConfig2 InvokeUIFromConfigBlob (NapCommon. h)
description: Viene implementato da convalida integrità sistema (SHV) in base alle esigenze per caricare la configurazione di un computer locale o remoto in memoria e visualizzare un'interfaccia utente che consente la manipolazione dei dati di configurazione.
ms.assetid: 9c012690-6751-4a47-8683-74abac610c77
keywords:
- NAP metodo InvokeUIFromConfigBlob
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
ms.openlocfilehash: 54cc1efaf7da3434e1aff10d57c2e175481a3d2d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103873566"
---
# <a name="inapcomponentconfig2invokeuifromconfigblob-method"></a>Metodo INapComponentConfig2:: InvokeUIFromConfigBlob

> [!Note]  
> La piattaforma protezione accesso alla rete non è disponibile a partire da Windows 10

 

Il metodo **InvokeUIFromConfigBlob** viene implementato da convalida integrità sistema (SHV) in base alle esigenze per caricare la configurazione di un computer locale o remoto in memoria e visualizzare un'interfaccia utente che consente la manipolazione dei dati di configurazione. Il componente di configurazione deve supportare l'utilizzo di [**INapComponentConfig**](inapcomponentconfig.md) tramite DCOM.

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

*hwndParent* \[ in\]
</dt> <dd>

Handle per la finestra padre o proprietario. È necessario specificare un handle di finestra valido.

</dd> <dt>

*inbCount* \[ in\]
</dt> <dd>

Dimensione in byte di *indata*.

</dd> <dt>

*indata* \[ in\]
</dt> <dd>

Puntatore a un buffer che archivia i dati di configurazione iniziali. Questi dati vengono esportati dal computer locale o remoto.

</dd> <dt>

*outbCount* \[ out\]
</dt> <dd>

Dimensioni, in byte, dei *dati di OutData*.

</dd> <dt>

*dati OutData* \[ out\]
</dt> <dd>

Puntatore a un buffer che archivia i dati di configurazione modificati dall'interfaccia utente di configurazione di convalida integrità di sistema. Questi dati vengono importati dal computer locale o remoto.

</dd> <dt>

*fConfigChanged* \[ out\]
</dt> <dd>

Puntatore a un **bool** che è impostato su **true** se la configurazione è stata modificata durante l'operazione dell'interfaccia utente e **false** in caso contrario.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce \_ OK se ha esito positivo o uno dei codici di errore standard di Windows.

## <a name="remarks"></a>Commenti

Se usato per un computer locale, questa funzione può essere usata per la configurazione di convalida integrità di sistema per criterio. Consente di richiamare un'interfaccia utente di convalida integrità sistema e modificare una configurazione di convalida integrità di sistema esistente.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Nessuno supportato<br/>                                                                |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2008\]<br/>                                     |
| Intestazione<br/>                   | <dl> <dt>NapCommon. h</dt> </dl>   |
| IDL<br/>                      | <dl> <dt>NapCommon. idl</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**INapComponentConfig2**](inapcomponentconfig2.md)
</dt> </dl>

 

 





