---
description: Recupera informazioni su un assembly quando si usa codice gestito nel .NET Framework Common Language Runtime.
ms.assetid: 45dcdc6a-74df-4763-ba8b-82f604db78d4
title: Classe ClrAssemblyLocator (ComSvcs.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ClrAssemblyLocator
api_type:
- COM
ms.openlocfilehash: 78f041e8bdc614b1ac6007e21ffbf46ea4afe789a501bb1acefdd21263031859
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119129273"
---
# <a name="clrassemblylocator-class"></a>Classe ClrAssemblyLocator

Recupera informazioni su un assembly quando si usa codice gestito nel .NET Framework Common Language Runtime.

## <a name="when-to-implement"></a>Quando implementare

Questa classe viene implementata da COM+.



| Requisito | Valore |
|------------|-------------------------------------------------------|
| CLSID      | GUID \_ AssemblyLocator                                 |
| ProgID     | L"System.EnterpriseServices.Internal.AssemblyLocator" |
| Interfacce | [**IAssemblyLocator**](/windows/desktop/api/ComSvcs/nn-comsvcs-iassemblylocator)          |



 

## <a name="when-to-use"></a>Utilizzo

Usare questa classe per accedere ai metodi di [**IAssemblyLocator.**](/windows/desktop/api/ComSvcs/nn-comsvcs-iassemblylocator)

## <a name="remarks"></a>Commenti

Per creare questo oggetto, chiamare [**CoCreateInstance.**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance)

Per usare questa classe da Microsoft Visual Basic, aggiungere un riferimento alla libreria dei tipi dei servizi COM+. Un oggetto ClrAssemblyLocator può essere dichiarato usando "COMSVCSLib.ClrAssemblyLocator" come nome della classe.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows XP solo con \[ app desktop SP1\]<br/>                                 |
| Server minimo supportato<br/> | Windows Solo app desktop di Server 2003 \[\]<br/>                                 |
| Intestazione<br/>                   | <dl> <dt>ComSvcs.h</dt> </dl> |



 

