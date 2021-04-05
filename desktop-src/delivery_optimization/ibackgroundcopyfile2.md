---
title: Interfaccia IBackgroundCopyFile2 (Deliveryoptimization. h)
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
ms.openlocfilehash: 4a866c8f18ee1dfb57f32ac3b2b9999e10106522
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104048276"
---
# <a name="ibackgroundcopyfile2-interface"></a>Interfaccia IBackgroundCopyFile2

Usare l'interfaccia **IBackgroundCopyFile2** per specificare un nuovo nome remoto per il file e recuperare l'elenco di intervalli da scaricare.

L'interfaccia **IBackgroundCopyFile2** eredita dall'interfaccia [**IBackgroundCopyFile**](ibackgroundcopyfile.md) .

Per ottenere un puntatore a interfaccia **IBackgroundCopyFile2** , chiamare il metodo **IBackgroundCopyFile:: QueryInterface** usando __uuidof (IBackgroundCopyFile2) per l'identificatore di interfaccia. Usare il puntatore all'interfaccia **IBackgroundCopyFile2** per chiamare entrambi i metodi [**IBackgroundCopyFile**](ibackgroundcopyfile.md) e **IBackgroundCopyFile2** .

## <a name="members"></a>Membri

L'interfaccia **IBackgroundCopyFile2** eredita da [**IBackgroundCopyFile**](ibackgroundcopyfile.md). **IBackgroundCopyFile2** dispone anche di questi tipi di membri:

-   [Metodi](#methods)

### <a name="methods"></a>Metodi

L'interfaccia **IBackgroundCopyFile2** dispone di questi metodi.



| Metodo                                                             | Descrizione                                                                      |
|:-------------------------------------------------------------------|:---------------------------------------------------------------------------------|
| [**GetFileRanges**](ibackgroundcopyfile2-getfileranges-method.md) | Recupera la matrice di intervalli che si desidera scaricare dall'URL.<br/> |
| [**Seremotename**](ibackgroundcopyfile2-setremotename-method.md) | Consente di modificare il nome remoto in un nuovo URL.<br/>                                 |



 

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-----------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Solo app desktop Windows 10 versione 1709 \[\]<br/>                                           |
| Server minimo supportato<br/> | Windows Server, versione 1709 \[ solo per le app desktop\]<br/>                                       |
| Intestazione<br/>                   | <dl> <dt>Deliveryoptimization. h</dt> </dl>   |
| IDL<br/>                      | <dl> <dt>DeliveryOptimization. idl</dt> </dl> |
| Libreria<br/>                  | <dl> <dt>Dosvc. lib</dt> </dl>                |
| DLL<br/>                      | <dl> <dt>Dosvc.dll</dt> </dl>                |
| IID<br/>                      | IID_IBackgroundCopyFile2 viene definito come 83E81B93-0873-474D-8A8C-F2018B1A939C<br/>             |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**IBackgroundCopyFile**](ibackgroundcopyfile.md)
</dt> </dl>

 

 





