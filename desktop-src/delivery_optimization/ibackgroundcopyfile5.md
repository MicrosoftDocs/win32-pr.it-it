---
title: Interfaccia IBackgroundCopyFile5 (Deliveryoptimization.h)
description: Usare questa interfaccia per ottenere o impostare le proprietà generiche dei trasferimenti Ottimizzazione recapito di file do(DO).
ms.assetid: 2D729717-62D2-4C69-92FE-F4289EC48DF1
keywords:
- Interfaccia IBackgroundCopyFile5
- Interfaccia IBackgroundCopyFile5, descritta
topic_type:
- apiref
api_name:
- IBackgroundCopyFile5
api_location:
- dosvc.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 369afa2f242faf1572b16f82aebc4ae18a8d501b5e3b806d74bb580beab3aa26
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119610361"
---
# <a name="ibackgroundcopyfile5-interface"></a>Interfaccia IBackgroundCopyFile5

Usare questa interfaccia per ottenere o impostare le proprietà generiche dei trasferimenti Ottimizzazione recapito di file do(DO).

Per ottenere un puntatore a interfaccia **IBackgroundCopyFile5,** chiamare il metodo **IBackgroundCopyFile::QueryInterface** usando __uuidof(IBackgroundCopyFile5) per l'identificatore di interfaccia.

## <a name="members"></a>Membri

**L'interfaccia IBackgroundCopyFile5** eredita dall'interfaccia [**IUnknown.**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) **IBackgroundCopyFile5** include anche questi tipi di membri:

-   [Metodi](#methods)

### <a name="methods"></a>Metodi

**L'interfaccia IBackgroundCopyFile5** include questi metodi.



| Metodo                                                  | Descrizione                                                         |
|:--------------------------------------------------------|:--------------------------------------------------------------------|
| [**Getproperty**](ibackgroundcopyfile5-getproperty.md) | Ottiene il valore di una proprietà BackgroundCopyFile generica.<br/> |
| [**SetProperty**](ibackgroundcopyfile5-setproperty.md) | Imposta il valore di una proprietà BackgroundCopyFile generica.<br/> |



 

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-----------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 10, solo app desktop versione 1709 \[\]<br/>                                           |
| Server minimo supportato<br/> | Windows Server, solo app desktop versione 1709 \[\]<br/>                                       |
| Intestazione<br/>                   | <dl> <dt>Deliveryoptimization.h</dt> </dl>   |
| Idl<br/>                      | <dl> <dt>DeliveryOptimization.idl</dt> </dl> |
| Libreria<br/>                  | <dl> <dt>Dosvc.lib</dt> </dl>                |
| DLL<br/>                      | <dl> <dt>Dosvc.dll</dt> </dl>                |
| IID<br/>                      | IID_IBackgroundCopyFile5 è definito come 85C1657F-DAFC-40E8-8834-DF18EA25717E<br/>             |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**IBackgroundCopyFile**](ibackgroundcopyfile.md)
</dt> <dt>

[**IBackgroundCopyFile2**](ibackgroundcopyfile2.md)
</dt> </dl>

 

