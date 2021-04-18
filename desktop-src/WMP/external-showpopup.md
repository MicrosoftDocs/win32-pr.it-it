---
title: External. showPopup, metodo
description: Si noti che in questo argomento viene descritta la funzionalità progettata per l'utilizzo da punti vendita online. | External. showPopup, metodo
ms.assetid: 17958543-dbed-45a5-9b02-4800a07cb820
keywords:
- Metodo showPopup Windows Media Player
- Metodo showPopup Windows Media Player, classe esterna
- Classe esterna Media Player Windows, metodo showPopup
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
ms.openlocfilehash: acaecb559e7df60067e89ec754ec9432233500f4
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106326008"
---
# <a name="externalshowpopup-method"></a>External. showPopup, metodo

> [!Note]  
> Questo argomento descrive la funzionalità progettata per l'uso da punti vendita online. L'uso di questa funzionalità al di fuori del contesto di un archivio online non è supportato.

 

Il metodo **ShowPopup** indica a Windows Media Player di visualizzare una pagina Web popup. ovvero una pagina Web visualizzata in una finestra separata.

## <a name="syntax"></a>Sintassi


```JScript
External.showPopup(
  PopupIndex,
  Parameters
)
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*PopupIndex* \[ in\]
</dt> <dd>

**Numero** (**Long**) che specifica l'indice della pagina Web popup.

</dd> <dt>

*Parametri* \[ di in\]
</dt> <dd>

**Stringa** che Windows Media Player aggiunge all'URL della pagina Web.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Questo metodo non restituisce valori.

## <a name="remarks"></a>Commenti

L'indice popup non è interpretato da Windows Media Player. Gli indici che identificano le pagine Web popup vengono creati dallo Store online e hanno un significato solo per lo Store online.

Nei passaggi seguenti viene illustrato il modo in cui Windows Media Player utilizza i parametri del metodo **ShowPopup** per creare un URL per la finestra popup.

1.  Script in una pagina di individuazione chiama **ShowPopup**, passando un Integer in *PopupIndex* e una stringa in *Parameters*.

2.  Windows Media Player passa l'indice a [IWMPContentPartner:: GetItemInfo](/previous-versions/windows/desktop/api/contentpartner/nf-contentpartner-iwmpcontentpartner-getiteminfo) per recuperare l'URL della pagina Web da visualizzare.

3.  Windows Media Player aggiunge i *parametri* all'URL come stringa di query. Se, ad esempio, **GetItemInfo** restituisce " https://www.Proseware.com/Pages/Popup1.htm " e *Parameters* è uguale a "DlgX = 800&DlgY = 400&Greeting = Hi", Windows Media Player crea l'URL seguente:

    https://www.Proseware.com/Pages/Popup1.htm?DlgX=800&DlgY=400&Greeting=Hi

È possibile usare i *parametri* per specificare le dimensioni della finestra popup. Se ad esempio si impostano i *parametri* su "DlgX = 800&DlgY = 400", la finestra popup avrà una dimensione di 800 pixel per 400 pixel.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|------------------------------------------------------------------------------------|
| Versione<br/> | Windows Media Player 11<br/>                                                 |
| DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Oggetto esterno per i negozi di tipo 1 online**](external-object-for-type-1-online-stores.md)
</dt> </dl>

 

 





