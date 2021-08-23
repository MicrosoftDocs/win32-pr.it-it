---
title: Metodo External.showPopup
description: Nota In questo argomento vengono descritte le funzionalità progettate per l'uso da parte dei negozi online. | Metodo External.showPopup
ms.assetid: 17958543-dbed-45a5-9b02-4800a07cb820
keywords:
- Metodo showPopup Windows Media Player
- Metodo showPopup Windows Media Player , classe External
- Classe esterna Windows Media Player, metodo showPopup
topic_type:
- apiref
api_name:
- External.showPopup
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a651add93e32c1c2eb82827a4089a338341f2506ba26d9fbb06061aa6d185d75
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119648342"
---
# <a name="externalshowpopup-method"></a>Metodo External.showPopup

> [!Note]  
> Questo argomento descrive le funzionalità progettate per l'uso da parte dei negozi online. L'uso di questa funzionalità all'esterno del contesto di un negozio online non è supportato.

 

Il **metodo showPopup** indica Windows Media Player visualizzare una pagina Web popup. una pagina Web visualizzata in una finestra separata.

## <a name="syntax"></a>Sintassi


```JScript
External.showPopup(
  PopupIndex,
  Parameters
)
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*PopupIndex* \[ Pollici\]
</dt> <dd>

**Numero** (**long**) che specifica l'indice della pagina Web popup.

</dd> <dt>

*Parametri* \[ Pollici\]
</dt> <dd>

**Stringa** che Windows Media Player aggiunge all'URL della pagina Web.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Questo metodo non restituisce valori.

## <a name="remarks"></a>Commenti

L'indice popup non viene interpretato da Windows Media Player. Gli indici che identificano le pagine Web popup vengono creati dal negozio online e hanno significato solo per il negozio online.

La procedura seguente illustra Windows Media Player i parametri del **metodo showPopup** per creare un URL per la finestra popup.

1.  Lo script in una pagina di individuazione **chiama showPopup**, passando un numero intero in *PopupIndex* e una stringa in *Parameters*.

2.  Windows Media Player passa l'indice a [IWMPContentPartner::GetItemInfo](/previous-versions/windows/desktop/api/contentpartner/nf-contentpartner-iwmpcontentpartner-getiteminfo) per recuperare l'URL della pagina Web da visualizzare.

3.  Windows Media Player aggiunge Parametri *all'URL* come stringa di query. Ad esempio, se **GetItemInfo** restituisce " " e Parameters è uguale https://www.Proseware.com/Pages/Popup1.htm a  "DlgX=800&DlgY=400&Greeting=Hi", Windows Media Player crea l'URL seguente:

    https://www.Proseware.com/Pages/Popup1.htm?DlgX=800&DlgY=400&Greeting=Hi

È possibile usare *Parametri* per specificare le dimensioni della finestra popup. Ad esempio, se  si imposta Parametri su "DlgX=800&DlgY=400", la finestra popup avrà dimensioni di 800 pixel per 400 pixel.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|------------------------------------------------------------------------------------|
| Versione<br/> | Windows Media Player 11<br/>                                                 |
| DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Oggetto esterno per i negozi online di tipo 1**](external-object-for-type-1-online-stores.md)
</dt> </dl>

 

 





