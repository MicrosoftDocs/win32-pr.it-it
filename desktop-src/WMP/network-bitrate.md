---
title: Network.bitRate
description: La proprietà bitRate recupera la velocità in bit corrente ricevuta.
ms.assetid: e970a43a-1773-4dc0-ac2f-115f698bc1f4
keywords:
- Network.bitRate Windows Media Player
topic_type:
- apiref
api_name:
- Network.bitRate
api_location:
- wmp.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ec142885bdd718903e956f8e86b59c3753cb024ecccc5efb2f8494797ea6a818
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119901781"
---
# <a name="networkbitrate"></a>Network.bitRate

La **proprietà bitRate** recupera la velocità in bit corrente ricevuta.

## <a name="syntax"></a>Sintassi

*lettore*. *rete*. **bitRate**

## <a name="possible-values"></a>Valori possibili

Questa proprietà è un numero di sola **lettura** (**long**).

## <a name="remarks"></a>Commenti

Questo valore è una combinazione delle velocità in bit dei flussi video e audio correnti.

## <a name="examples"></a>Esempio

Nell'esempio JScript seguente viene utilizzata *la rete*. **bitRate** per visualizzare la velocità in bit del supporto corrente. Le informazioni vengono visualizzate in un DIV HTML creato con ID = "BR". **L'oggetto** Player è stato creato con ID = "Player".


```JScript
<!<entity type="mdash"/>-Create an event handler. -->
<SCRIPT FOR = Player EVENT = PlayStateChange()>
   switch (Player.playState){

      case 3:

         if (Player.network.bitRate){

            BR.innerHTML = "Current Bit Rate: " + Player.network.bitRate;
            BR.innerHTML += " K bits/second";
          }

         break;

      default:
   }
</SCRIPT>

```



## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|------------------------------------------------------------------------------------|
| Versione<br/> | Windows Media Player versione 7.0 o successiva.<br/>                              |
| DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Oggetto di rete**](network-object.md)
</dt> </dl>

 

 





