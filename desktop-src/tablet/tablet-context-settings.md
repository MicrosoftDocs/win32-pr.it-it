---
description: Contiene informazioni utilizzate nella creazione di un contesto tablet.
ms.assetid: 10466c23-f4cb-4205-886b-d85a2f530afe
title: TABLET_CONTEXT_SETTINGS struttura
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
ms.openlocfilehash: 75634cd635773ff0b009860256b1147c31ee43dde200586e12713a707aa999b6
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119335081"
---
# <a name="tablet_context_settings-structure"></a>Struttura TABLET \_ CONTEXT \_ SETTINGS

Contiene informazioni utilizzate nella creazione di un contesto tablet.

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

Identificatori univoci per le proprietà del pacchetto.

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

Maschera del pulsante verso l'alto.

</dd> <dt>

**lXMargin**
</dt> <dd>

Margine della direzione X.

</dd> <dt>

**lYMargin**
</dt> <dd>

Margine di direzione Y.

</dd> </dl>

## <a name="remarks"></a>Commenti

In genere, un'applicazione ottiene i valori predefiniti dal metodo [**ITablet::GetDefaultContextSettings**](itablet-getdefaultcontextsettings.md), modifica i valori in base alle proprie esigenze e quindi passa la struttura delle impostazioni modificata al metodo [**ITablet::CreateContext**](itablet-createcontext.md).

Questa struttura determina quali eventi otterrà un'applicazione, come verranno elaborati e come verranno recapitati all'applicazione o Windows se stessa.

Le maschere dei pulsanti determinano insieme i tipi di eventi che verranno elaborati dal contesto.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo app desktop tablet PC Edition \[ XP\]<br/> |
| Server minimo supportato<br/> | Nessuno supportato<br/>                                     |



 

 




