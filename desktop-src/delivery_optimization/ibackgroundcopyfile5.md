---
title: Interfaccia IBackgroundCopyFile5 (Deliveryoptimization. h)
description: Usare questa interfaccia per ottenere o impostare le proprietà generiche dei trasferimenti di file di ottimizzazione recapito.
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
ms.openlocfilehash: 2f23fdb99ba24b4faeca7a65930bf83d4634a979
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104119611"
---
# <a name="ibackgroundcopyfile5-interface"></a>Interfaccia IBackgroundCopyFile5

Usare questa interfaccia per ottenere o impostare le proprietà generiche dei trasferimenti di file di ottimizzazione recapito.

Per ottenere un puntatore a interfaccia **IBackgroundCopyFile5** , chiamare il metodo **IBackgroundCopyFile:: QueryInterface** usando __uuidof (IBackgroundCopyFile5) per l'identificatore di interfaccia.

## <a name="members"></a>Membri

L'interfaccia **IBackgroundCopyFile5** eredita dall'interfaccia [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) . **IBackgroundCopyFile5** dispone anche di questi tipi di membri:

-   [Metodi](#methods)

### <a name="methods"></a>Metodi

L'interfaccia **IBackgroundCopyFile5** dispone di questi metodi.



| Metodo                                                  | Descrizione                                                         |
|:--------------------------------------------------------|:--------------------------------------------------------------------|
| [**GetProperty**](ibackgroundcopyfile5-getproperty.md) | Ottiene il valore di una proprietà BackgroundCopyFile generica.<br/> |
| [**SetProperty**](ibackgroundcopyfile5-setproperty.md) | Imposta il valore di una proprietà BackgroundCopyFile generica.<br/> |



 

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-----------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Solo app desktop Windows 10 versione 1709 \[\]<br/>                                           |
| Server minimo supportato<br/> | Windows Server, versione 1709 \[ solo per le app desktop\]<br/>                                       |
| Intestazione<br/>                   | <dl> <dt>Deliveryoptimization. h</dt> </dl>   |
| IDL<br/>                      | <dl> <dt>DeliveryOptimization. idl</dt> </dl> |
| Libreria<br/>                  | <dl> <dt>Dosvc. lib</dt> </dl>                |
| DLL<br/>                      | <dl> <dt>Dosvc.dll</dt> </dl>                |
| IID<br/>                      | IID_IBackgroundCopyFile5 viene definito come 85C1657F-DAFC-40E8-8834-DF18EA25717E<br/>             |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**IBackgroundCopyFile**](ibackgroundcopyfile.md)
</dt> <dt>

[**IBackgroundCopyFile2**](ibackgroundcopyfile2.md)
</dt> </dl>

 

