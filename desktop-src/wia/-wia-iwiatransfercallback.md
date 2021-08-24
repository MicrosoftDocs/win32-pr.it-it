---
description: L'interfaccia IWiaTransferCallback riceve i callback durante un trasferimento dei dati.
ms.assetid: 8fcaccf5-4d7b-4984-97ec-ec8c838a8360
title: Interfaccia IWiaTransferCallback (Wia.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWiaTransferCallback
api_type:
- COM
api_location:
- Wiaguid.lib
- Wiaguid.dll
ms.openlocfilehash: 20c577530785de3e05d00d4674556fbcd03cb69832b164e12dc703108d23c58a
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119549641"
---
# <a name="iwiatransfercallback-interface"></a>Interfaccia IWiaTransferCallback

**L'interfaccia IWiaTransferCallback** riceve i callback durante un trasferimento dei dati.

## <a name="members"></a>Membri

**L'interfaccia IWiaTransferCallback** eredita dall'interfaccia [**IUnknown.**](/windows/win32/api/unknwn/nn-unknwn-iunknown) **IWiaTransferCallback** include anche questi tipi di membri:

-   [Metodi](#methods)

### <a name="methods"></a>Metodi

**L'interfaccia IWiaTransferCallback** include questi metodi.



| Metodo                                                                 | Descrizione                                                              |
|:-----------------------------------------------------------------------|:-------------------------------------------------------------------------|
| [**GetNextStream**](-wia-iwiatransfercallback-getnextstream.md)       | Ottiene un nuovo flusso per l'elemento specificato. <br/>                    |
| [**TransferCallback**](-wia-iwiatransfercallback-transfercallback.md) | Fornisce lo stato di avanzamento e altre notifiche durante un trasferimento. <br/> |



 

## <a name="remarks"></a>Commenti

Gli sviluppatori di filtri di elaborazione delle immagini devono implementare questa interfaccia e [**l'interfaccia IWiaImageFilter.**](-wia-iwiaimagefilter.md)

**L'interfaccia IWiaTransferCallback,** come tutte le Component Object Model (COM), eredita i metodi dell'interfaccia [IUnknown.](/windows/win32/api/unknwn/nn-unknwn-iunknown)



| Metodi IUnknown                                        | Descrizione                               |
|---------------------------------------------------------|-------------------------------------------|
| [IUnknown::QueryInterface](/windows/win32/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) | Restituisce puntatori alle interfacce supportate. |
| [IUnknown::AddRef](/windows/win32/api/unknwn/nf-unknwn-iunknown-addref)                 | Incrementa il conteggio dei riferimenti.               |
| [IUnknown::Release](/windows/win32/api/unknwn/nf-unknwn-iunknown-release)               | Riduce il conteggio dei riferimenti.               |



 

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo \[ app desktop Vista\]<br/>                                         |
| Server minimo supportato<br/> | Windows Solo app desktop di Server 2008 \[\]<br/>                                   |
| Intestazione<br/>                   | <dl> <dt>Wia.h</dt> </dl>       |
| Idl<br/>                      | <dl> <dt>Wia.idl</dt> </dl>     |
| Libreria<br/>                  | <dl> <dt>Wiaguid.lib</dt> </dl> |



 

 
