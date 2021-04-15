---
title: Interfaccia IResultType (WdsSharedIDL. h)
description: Espone informazioni sul tipo di proprietà.
ms.assetid: 68abd470-2505-4836-a17f-f1c14157f8e7
keywords:
- Funzionalità dell'ambiente Windows legacy dell'interfaccia IResultType
- Funzionalità dell'ambiente Windows legacy dell'interfaccia IResultType, descritte
topic_type:
- apiref
api_name:
- IResultType
api_location:
- WdsSharedIDL.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 88451739a6ca2eb600838ea137ebc1ddba98f3a8
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104476127"
---
# <a name="iresulttype-interface"></a>Interfaccia IResultType

> [!NOTE]
> Windows Desktop Search 2. x è una tecnologia obsoleta originariamente disponibile come componente aggiuntivo per Windows XP e Windows Server 2003. Nelle versioni successive usare invece l' [API di ricerca di Windows](../search/-search-reference-entry-page.md) . 

Espone informazioni sul tipo di proprietà.

## <a name="members"></a>Membri

L'interfaccia **IResultType** eredita dall'interfaccia [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) . **IResultType** dispone anche di questi tipi di membri:

-   [Proprietà](#properties)

### <a name="properties"></a>Proprietà

L'interfaccia **IResultType** ha queste proprietà.



| Proprietà                                                                 | Tipo di accesso           | Descrizione                                                                           |
|:-------------------------------------------------------------------------|:----------------------|:--------------------------------------------------------------------------------------|
| [**DisplayName**](-search-2x-iresulttype-displayname.md)<br/>     | Sola lettura<br/>  | Nome visualizzato localizzato del tipo:<br/>                                        |
| [**GetProperty**](-search-2x-iresulttype-getproperty.md)<br/>     | Lettura/Scrittura<br/> | Questa proprietà contiene informazioni sulle proprietà specificate. <br/>                    |
| [**PreceivedType**](-search-2x-iresulttype-preceivedtype.md)<br/> | Sola lettura<br/>  | Questa proprietà contiene la stringa utilizzata per identificare il tipo nell'indice. <br/> |
| [**PropertyCount**](-search-2x-iresulttype-propertycount.md)<br/> | Sola lettura<br/>  | Questa proprietà contiene il numero di proprietà esposte dal tipo. <br/>      |
| [**UID**](-search-2x-iresulttype-uid.md)<br/>                     | Sola lettura<br/>  | Questa proprietà contiene l'identificatore univoco per il tipo. <br/>                |



 

## <a name="remarks"></a>Commenti

Questi metodi espongono i tipi di informazioni restituite.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Solo app desktop Windows XP con SP2 \[\]<br/>                                      |
| Server minimo supportato<br/> | Windows Server 2003 con \[ solo app desktop SP1\]<br/>                             |
| Componente ridistribuibile<br/>          | Windows Desktop Search (WDS) 3,0<br/>                                               |
| Intestazione<br/>                   | <dl> <dt>WdsSharedIDL. h</dt> </dl> |



 

