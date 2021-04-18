---
title: Interfaccia IEnumBackgroundCopyFiles (Deliveryoptimization. h)
description: Utilizzare l'interfaccia IEnumBackgroundCopyFiles per enumerare i file contenuti in un processo. Per ottenere un puntatore a interfaccia IEnumBackgroundCopyFiles, chiamare il metodo Metodo ibackgroundcopyjob EnumFiles.
ms.assetid: 539973BA-2756-4163-9D8B-4B7C0A708A8D
keywords:
- Interfaccia IEnumBackgroundCopyFiles
- Interfaccia IEnumBackgroundCopyFiles, descritta
topic_type:
- apiref
api_name:
- IEnumBackgroundCopyFiles
api_location:
- dosvc.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 7e46e94139a0c82e6c5b45f9397d76de8b4fdb43
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "106301591"
---
# <a name="ienumbackgroundcopyfiles-interface"></a>Interfaccia IEnumBackgroundCopyFiles

Utilizzare l'interfaccia **IEnumBackgroundCopyFiles** per enumerare i file contenuti in un processo. Per ottenere un puntatore a interfaccia **IEnumBackgroundCopyFiles** , chiamare il metodo [**Metodo ibackgroundcopyjob:: EnumFiles**](ibackgroundcopyjob-enumfiles.md) .

## <a name="members"></a>Membri

L'interfaccia **IEnumBackgroundCopyFiles** eredita dall'interfaccia [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) . **IEnumBackgroundCopyFiles** dispone anche di questi tipi di membri:

-   [Metodi](#methods)

### <a name="methods"></a>Metodi

L'interfaccia **IEnumBackgroundCopyFiles** dispone di questi metodi.



| Metodo                                                | Descrizione                                                                   |
|:------------------------------------------------------|:------------------------------------------------------------------------------|
| [**GetCount**](ienumbackgroundcopyfiles-getcount.md) | Recupera il numero di elementi nell'enumerazione.<br/>                  |
| [**Avanti**](ienumbackgroundcopyfiles-next.md)         | Recupera un determinato numero di elementi nella sequenza di enumerazione.<br/> |
| [**Reset**](ienumbackgroundcopyfiles-reset.md)       | Riporta all'inizio la sequenza di enumerazione.<br/>                  |
| [**Ignora**](ienumbackgroundcopyfiles-skip.md)         | Ignora un determinato numero di elementi nella sequenza di enumerazione.<br/>     |



 

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-----------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Solo app desktop Windows 10 versione 1709 \[\]<br/>                                           |
| Server minimo supportato<br/> | Windows Server, versione 1709 \[ solo per le app desktop\]<br/>                                       |
| Intestazione<br/>                   | <dl> <dt>Deliveryoptimization. h</dt> </dl>   |
| IDL<br/>                      | <dl> <dt>DeliveryOptimization. idl</dt> </dl> |
| Libreria<br/>                  | <dl> <dt>Dosvc. lib</dt> </dl>                |
| DLL<br/>                      | <dl> <dt>Dosvc.dll</dt> </dl>                |
| IID<br/>                      | IID_IEnumBackgroundCopyFiles viene definito come CA51E165-C365-424C-8D41-24AAA4FF3C40<br/>         |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Metodo ibackgroundcopyjob:: EnumFiles**](ibackgroundcopyjob-enumfiles.md)
</dt> </dl>

 

