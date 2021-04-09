---
description: Contiene informazioni utilizzate per la creazione di un contesto di Tablet.
ms.assetid: 10466c23-f4cb-4205-886b-d85a2f530afe
title: Struttura TABLET_CONTEXT_SETTINGS
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- TABLET_CONTEXT_SETTINGS
api_type:
- NA
api_location: ''
ms.openlocfilehash: 9357281409ed4c48b4c6013a7a2be2997d58b094
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "103968607"
---
# <a name="tablet_context_settings-structure"></a>\_ \_ Struttura delle impostazioni di contesto del Tablet

Contiene informazioni utilizzate per la creazione di un contesto di Tablet.

## <a name="syntax"></a>Sintassi


```C++
typedef struct _TABLET_CONTEXT_SETTINGS {
  ULONG cPktProps;
  GUID  *pguidPktProps;
  ULONG cPktBtns;
  GUID  *pguidPktBtns;
  DWORD *pdwBtnDnMask;
  DWORD *pdwBtnUpMask;
  LONG  lXMargin;
  LONG  lYMargin;
} TABLET_CONTEXT_SETTINGS;
```



## <a name="members"></a>Members

<dl> <dt>

**cPktProps**
</dt> <dd>

Numero di proprietà in un pacchetto.

</dd> <dt>

**pguidPktProps**
</dt> <dd>

Identificatori univoci per le proprietà dei pacchetti.

</dd> <dt>

**cPktBtns**
</dt> <dd>

Numero di pulsanti.

</dd> <dt>

**pguidPktBtns**
</dt> <dd>

Identificatori univoci per i pulsanti.

</dd> <dt>

**pdwBtnDnMask**
</dt> <dd>

Maschera del pulsante verso il basso.

</dd> <dt>

**pdwBtnUpMask**
</dt> <dd>

Maschera del pulsante su.

</dd> <dt>

**lXMargin**
</dt> <dd>

Margine della direzione X.

</dd> <dt>

**lYMargin**
</dt> <dd>

Margine della direzione Y.

</dd> </dl>

## <a name="remarks"></a>Commenti

In genere, un'applicazione ottiene i valori predefiniti dal [**Metodo ITablet:: GetDefaultContextSettings**](itablet-getdefaultcontextsettings.md), modifica i valori in base alle proprie esigenze e quindi passa la struttura delle impostazioni modificate al [**Metodo ITablet:: CreateContext**](itablet-createcontext.md).

Questa struttura determina gli eventi che un'applicazione otterrà, il modo in cui verranno elaborati e il modo in cui verranno recapitati all'applicazione o a Windows.

Le maschere dei pulsanti stabiliscono insieme i tipi di eventi che verranno elaborati dal contesto.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------|
| Client minimo supportato<br/> | Solo app desktop Windows XP Tablet PC Edition \[\]<br/> |
| Server minimo supportato<br/> | Nessuno supportato<br/>                                     |



 

 




