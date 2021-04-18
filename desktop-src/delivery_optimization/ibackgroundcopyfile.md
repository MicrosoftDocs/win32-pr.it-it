---
title: Interfaccia IBackgroundCopyFile (Deliveryoptimization. h)
description: IBackgroundCopyFile contiene informazioni su un file che fa parte di un processo. È ad esempio possibile utilizzare i metodi IBackgroundCopyFile per recuperare i nomi locali e remoti del file e trasferire le informazioni sullo stato di avanzamento.
ms.assetid: 463ED61A-D7C5-4B44-97CF-FDAA138CE9E3
keywords:
- Interfaccia IBackgroundCopyFile
- Interfaccia IBackgroundCopyFile, descritta
topic_type:
- apiref
api_name:
- IBackgroundCopyFile
api_location:
- dosvc.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 3e4a54a66dee87770326d2456cb384e9d77f15e6
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "106301484"
---
# <a name="ibackgroundcopyfile-interface"></a>Interfaccia IBackgroundCopyFile

**IBackgroundCopyFile** contiene informazioni su un file che fa parte di un processo. È ad esempio possibile utilizzare i metodi **IBackgroundCopyFile** per recuperare i nomi locali e remoti del file e trasferire le informazioni sullo stato di avanzamento.

Per ottenere un puntatore a interfaccia **IBackgroundCopyFile** , chiamare il metodo [**IBackgroundCopyError:: GetFile**](ibackgroundcopyerror-getfile-method.md) o il metodo [**IEnumBackgroundCopyFiles:: Next**](ienumbackgroundcopyfiles-next.md) .

## <a name="members"></a>Membri

L'interfaccia **IBackgroundCopyFile** eredita dall'interfaccia [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) . **IBackgroundCopyFile** dispone anche di questi tipi di membri:

-   [Metodi](#methods)

### <a name="methods"></a>Metodi

L'interfaccia **IBackgroundCopyFile** dispone di questi metodi.



| Metodo                                                            | Descrizione                                             |
|:------------------------------------------------------------------|:--------------------------------------------------------|
| [**GetLocalName**](ibackgroundcopyfile-getlocalname-method.md)   | Recupera il nome locale del file.<br/>        |
| [**GetProgress**](ibackgroundcopyfile-getprogress-method.md)     | Recupera lo stato di avanzamento del trasferimento di file.<br/> |
| [**GetRemoteName**](ibackgroundcopyfile-getremotename-method.md) | Recupera il nome remoto del file.<br/>       |



 

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-----------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Solo app desktop Windows 10 versione 1709 \[\]<br/>                                           |
| Server minimo supportato<br/> | Windows Server, versione 1709 \[ solo per le app desktop\]<br/>                                       |
| Intestazione<br/>                   | <dl> <dt>Deliveryoptimization. h</dt> </dl>   |
| IDL<br/>                      | <dl> <dt>DeliveryOptimization. idl</dt> </dl> |
| Libreria<br/>                  | <dl> <dt>Dosvc. lib</dt> </dl>                |
| DLL<br/>                      | <dl> <dt>Dosvc.dll</dt> </dl>                |
| IID<br/>                      | IID_IBackgroundCopyFile viene definito come 01B7BD23-FB88-4A77-8490-5891D3E4653A<br/>              |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**IBackgroundCopyError**](ibackgroundcopyerror.md)
</dt> <dt>

[**IBackgroundCopyFile2**](ibackgroundcopyfile2.md)
</dt> <dt>

[**Metodo ibackgroundcopyjob**](ibackgroundcopyjob-.md)
</dt> <dt>

[**IEnumBackgroundCopyFiles**](ienumbackgroundcopyfiles-.md)
</dt> </dl>

 

