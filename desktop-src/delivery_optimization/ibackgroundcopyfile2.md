---
title: Interfaccia IBackgroundCopyFile2 (Deliveryoptimization.h)
description: Usare l'interfaccia IBackgroundCopyFile2 per specificare un nuovo nome remoto per il file e recuperare l'elenco di intervalli da scaricare.
ms.assetid: 28233310-9F2A-4567-B0B1-B549F862F3C8
keywords:
- Interfaccia IBackgroundCopyFile2
- Interfaccia IBackgroundCopyFile2, descritta
topic_type:
- apiref
api_name:
- IBackgroundCopyFile2
api_location:
- dosvc.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 0f185fef1ddaa9ceb4298f3e8916bb3d207b311b300f0071d601aadf47b0777a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119853861"
---
# <a name="ibackgroundcopyfile2-interface"></a>Interfaccia IBackgroundCopyFile2

Usare **l'interfaccia IBackgroundCopyFile2** per specificare un nuovo nome remoto per il file e recuperare l'elenco di intervalli da scaricare.

**L'interfaccia IBackgroundCopyFile2** eredita dall'interfaccia [**IBackgroundCopyFile.**](ibackgroundcopyfile.md)

Per ottenere un puntatore a interfaccia **IBackgroundCopyFile2,** chiamare il metodo **IBackgroundCopyFile::QueryInterface** usando __uuidof(IBackgroundCopyFile2) per l'identificatore di interfaccia. Usare il puntatore a interfaccia **IBackgroundCopyFile2** per chiamare entrambi i metodi [**IBackgroundCopyFile**](ibackgroundcopyfile.md) e **IBackgroundCopyFile2.**

## <a name="members"></a>Membri

**L'interfaccia IBackgroundCopyFile2** eredita da [**IBackgroundCopyFile.**](ibackgroundcopyfile.md) **IBackgroundCopyFile2** include anche questi tipi di membri:

-   [Metodi](#methods)

### <a name="methods"></a>Metodi

**L'interfaccia IBackgroundCopyFile2** include questi metodi.



| Metodo                                                             | Descrizione                                                                      |
|:-------------------------------------------------------------------|:---------------------------------------------------------------------------------|
| [**GetFileRanges**](ibackgroundcopyfile2-getfileranges-method.md) | Recupera la matrice di intervalli da scaricare dall'URL.<br/> |
| [**SetRemoteName**](ibackgroundcopyfile2-setremotename-method.md) | Modifica il nome remoto in un nuovo URL.<br/>                                 |



 

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-----------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 10, solo app desktop versione 1709 \[\]<br/>                                           |
| Server minimo supportato<br/> | Windows Server, solo app desktop versione 1709 \[\]<br/>                                       |
| Intestazione<br/>                   | <dl> <dt>Deliveryoptimization.h</dt> </dl>   |
| Idl<br/>                      | <dl> <dt>DeliveryOptimization.idl</dt> </dl> |
| Libreria<br/>                  | <dl> <dt>Dosvc.lib</dt> </dl>                |
| DLL<br/>                      | <dl> <dt>Dosvc.dll</dt> </dl>                |
| IID<br/>                      | IID_IBackgroundCopyFile2 è definito come 83E81B93-0873-474D-8A8C-F2018B1A939C<br/>             |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**IBackgroundCopyFile**](ibackgroundcopyfile.md)
</dt> </dl>

 

 





