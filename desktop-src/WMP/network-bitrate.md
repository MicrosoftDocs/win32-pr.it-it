---
title: Rete. bitrate
description: La proprietà bitrate recupera la velocità in bit corrente ricevuta.
ms.assetid: e970a43a-1773-4dc0-ac2f-115f698bc1f4
keywords:
- Media Player Windows di rete. bitrate
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
ms.openlocfilehash: 4373d667ea41d55b5b0e12f1a47289f15d7b115b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106326120"
---
# <a name="networkbitrate"></a>Rete. bitrate

La proprietà **bitrate** recupera la velocità in bit corrente ricevuta.

## <a name="syntax"></a>Sintassi

*Player*. *rete*. **velocità in bit**

## <a name="possible-values"></a>Valori possibili

Questa proprietà è un **numero** di sola lettura (**Long**).

## <a name="remarks"></a>Commenti

Questo valore è una combinazione della velocità in bit dei flussi video e audio correnti.

## <a name="examples"></a>Esempio

Nell'esempio JScript seguente viene utilizzata la *rete*. **bitrate** per visualizzare la velocità in bit dei supporti correnti. Le informazioni vengono visualizzate in un DIV HTML creato con ID = "BR". L'oggetto **Player** è stato creato con ID = "Player".


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
| Versione<br/> | Windows Media Player versione 7,0 o successiva.<br/>                              |
| DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Oggetto di rete**](network-object.md)
</dt> </dl>

 

 





