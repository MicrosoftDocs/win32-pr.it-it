---
title: TBN_GETBUTTONINFO di notifica (Commctrl.h)
description: Recupera le informazioni di personalizzazione della barra degli strumenti e notifica alla finestra padre della barra degli strumenti le modifiche apportate alla barra degli strumenti. Questo codice di notifica viene inviato sotto forma di messaggio WM \_ NOTIFY.
ms.assetid: 088527fe-5a38-4c35-ba68-d0cbfdee410c
keywords:
- TBN_GETBUTTONINFO codice di notifica Windows controlli
topic_type:
- apiref
api_name:
- TBN_GETBUTTONINFO
- TBN_GETBUTTONINFOA
- TBN_GETBUTTONINFOW
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 32a73b7da3efee0b1bb1ba829cf40356e6060a5f7e7fdfcc2467e2cca32226a5
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119876861"
---
# <a name="tbn_getbuttoninfo-notification-code"></a>Codice di \_ notifica TBN GETBUTTONINFO

Recupera le informazioni di personalizzazione della barra degli strumenti e notifica alla finestra padre della barra degli strumenti le modifiche apportate alla barra degli strumenti. Questo codice di notifica viene inviato sotto forma di [**messaggio WM \_ NOTIFY.**](wm-notify.md)


```C++
TBN_GETBUTTONINFO 

    lpnmtb = (LPNMTOOLBAR) lParam; 
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*lParam* 
</dt> <dd>

Puntatore a [**una struttura NMTOOLBAR.**](/windows/win32/api/commctrl/ns-commctrl-nmtoolbara) Il **membro iItem** specifica un indice in base zero che fornisce un conteggio dei pulsanti visualizzati nella finestra di dialogo Personalizza barra degli strumenti come disponibili e presenti sulla barra degli strumenti. Il **membro pszText** specifica l'indirizzo del testo del pulsante corrente e **cchText** ne specifica la lunghezza in caratteri. L'applicazione deve riempire la struttura con informazioni sul pulsante.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce **TRUE se** le informazioni sul pulsante sono stati copiati nella struttura specificata oppure FALSE in caso **contrario.**

## <a name="remarks"></a>Commenti

Il controllo barra degli strumenti alloca un buffer e il ricevitore (finestra padre) deve copiare il testo in tale buffer. Il **membro cchText** contiene la lunghezza del buffer allocato dalla barra degli strumenti quando TBN \_ GETBUTTONINFO viene inviato alla finestra padre.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo \[ app desktop di Vista\]<br/>                                        |
| Server minimo supportato<br/> | Windows Solo app desktop server 2003 \[\]<br/>                                  |
| Intestazione<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |
| Nomi Unicode e ANSI<br/>   | **TBN \_ GETBUTTONINFOW** (Unicode) e **TBN \_ GETBUTTONINFOA** (ANSI)<br/>       |



 

 





