---
description: Espone i metodi usati per inizializzare un elenco usato più di recente (MRU) per un oggetto di completamento automatico.
title: Interfaccia IACLCustomMRU
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IACLCustomMRU
api_type:
- COM
api_location: ''
ms.assetid: 6ebf64da-9eba-4ea7-91aa-242474097be1
ms.openlocfilehash: 54cda8d6cc3c7f1c46d6bce7736160b0da67a4c0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104994624"
---
# <a name="iaclcustommru-interface"></a>Interfaccia IACLCustomMRU

Espone i metodi usati per inizializzare un elenco usato più di recente (MRU) per un oggetto di completamento automatico.

## <a name="members"></a>Membri

L'interfaccia **IACLCustomMRU** eredita dall'interfaccia [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) . **IACLCustomMRU** dispone anche di questi tipi di membri:

-   [Metodi](#methods)

### <a name="methods"></a>Metodi

L'interfaccia **IACLCustomMRU** dispone di questi metodi.



| Metodo                                             | Descrizione                                                             |
|:---------------------------------------------------|:------------------------------------------------------------------------|
| [**AddMRUString**](iaclcustommru-addmrustring.md) | Aggiunge una voce all'elenco MRU.<br/>                               |
| [**Inizializzare**](iaclcustommru-initialize.md)     | Carica un elenco di stringhe nell'elenco MRU dal registro di sistema.<br/> |



 

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop Windows XP\]<br/>          |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2003\]<br/> |



 

 
