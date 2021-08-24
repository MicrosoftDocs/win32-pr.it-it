---
title: Interfaccia IEnumBackgroundCopyFiles (Deliveryoptimization.h)
description: Usare l'interfaccia IEnumBackgroundCopyFiles per enumerare i file contenuti in un processo. Per ottenere un puntatore a interfaccia IEnumBackgroundCopyFiles, chiamare il metodo IBackgroundCopyJob EnumFiles.
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
ms.openlocfilehash: c6cf97975d583a99145e32482bc097ebd6ce3cc052e62560a34f7f78c1f88ae6
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119635681"
---
# <a name="ienumbackgroundcopyfiles-interface"></a>Interfaccia IEnumBackgroundCopyFiles

Usare **l'interfaccia IEnumBackgroundCopyFiles** per enumerare i file contenuti in un processo. Per ottenere un puntatore a **interfaccia IEnumBackgroundCopyFiles,** chiamare il [**metodo IBackgroundCopyJob::EnumFiles.**](ibackgroundcopyjob-enumfiles.md)

## <a name="members"></a>Membri

**L'interfaccia IEnumBackgroundCopyFiles** eredita dall'interfaccia [**IUnknown.**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) **IEnumBackgroundCopyFiles** include anche questi tipi di membri:

-   [Metodi](#methods)

### <a name="methods"></a>Metodi

**L'interfaccia IEnumBackgroundCopyFiles** include questi metodi.



| Metodo                                                | Descrizione                                                                   |
|:------------------------------------------------------|:------------------------------------------------------------------------------|
| [**GetCount**](ienumbackgroundcopyfiles-getcount.md) | Recupera il numero di elementi nell'enumerazione .<br/>                  |
| [**Avanti**](ienumbackgroundcopyfiles-next.md)         | Recupera un determinato numero di elementi nella sequenza di enumerazione.<br/> |
| [**Reset**](ienumbackgroundcopyfiles-reset.md)       | Riporta all'inizio la sequenza di enumerazione.<br/>                  |
| [**Ignora**](ienumbackgroundcopyfiles-skip.md)         | Ignora un determinato numero di elementi nella sequenza di enumerazione.<br/>     |



 

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-----------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 10, solo app desktop versione 1709 \[\]<br/>                                           |
| Server minimo supportato<br/> | Windows Server, solo app desktop versione 1709 \[\]<br/>                                       |
| Intestazione<br/>                   | <dl> <dt>Deliveryoptimization.h</dt> </dl>   |
| Idl<br/>                      | <dl> <dt>DeliveryOptimization.idl</dt> </dl> |
| Libreria<br/>                  | <dl> <dt>Dosvc.lib</dt> </dl>                |
| DLL<br/>                      | <dl> <dt>Dosvc.dll</dt> </dl>                |
| IID<br/>                      | IID_IEnumBackgroundCopyFiles è definito come CA51E165-C365-424C-8D41-24AAA4FF3C40<br/>         |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**IBackgroundCopyJob::EnumFiles**](ibackgroundcopyjob-enumfiles.md)
</dt> </dl>

 

