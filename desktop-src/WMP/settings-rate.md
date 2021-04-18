---
title: Settings. rate
description: La proprietà rate specifica o recupera la frequenza di riproduzione corrente dei supporti video.
ms.assetid: 0f95f7ac-1bb6-4c80-89eb-eb300a03a0f1
keywords:
- Impostazioni. Frequenza Media Player di Windows
topic_type:
- apiref
api_name:
- Settings.rate
api_location:
- wmp.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e61287789487fddbe7e77fba5fc033d3103aecb8
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106327371"
---
# <a name="settingsrate"></a>Settings. rate

La proprietà **rate** specifica o recupera la frequenza di riproduzione corrente dei supporti video.

## <a name="syntax"></a>Sintassi

Player. Settings. rate

## <a name="possible-values"></a>Valori possibili

Questa proprietà è un **numero** di lettura/scrittura (**Double**) il cui valore predefinito è 1,0.

## <a name="remarks"></a>Commenti

Questa proprietà funge da valore moltiplicatore che consente di riprodurre una clip a una velocità più veloce o più lenta. Il valore predefinito 1,0 indica la velocità creata. Si noti che una traccia audio diventa difficile da comprendere a una velocità inferiore a 0,5 o superiore a 1,5. Una velocità di riproduzione pari a 2 corrisponde al doppio della velocità di riproduzione normale.

Windows Media Player tenterà di utilizzare il più efficace di quattro diverse modalità di riproduzione. Queste modalità sono la riproduzione video uniforme con il pitch audio mantenuto e la riproduzione video uniforme con il pitch audio non mantenuto, la riproduzione video uniforme senza audio e la riproduzione di video con fotogrammi chiave senza audio. La modalità scelta dal lettore dipende da numerosi fattori, tra cui il tipo di file e la posizione, il sistema operativo, la rete e il server.

Si applicano anche altre considerazioni, a seconda del tipo di supporto:

-   File Windows Media Format (WMV) e ASF: i valori ottimali per questa proprietà sono compresi tra 1 e 10 o da 1 a 10 per la riproduzione inversa. I valori compresi tra 0,5 e 1,0 o da-0,5 a-1,0 possono anche funzionare correttamente nei casi in cui è possibile mantenere il pitch audio, ad esempio quando si giocano i file che si trovano nel computer locale. I valori con una grandezza assoluta maggiore di 10 sono consentiti, ma non sono molto significativi.
-   Altri tipi di supporti video: questa proprietà può variare da 0 a 9. I valori negativi non sono consentiti. I valori minori di 1 rappresentano un movimento lento. I valori superiori a 9 sono consentiti, ma non sono molto significativi.

*Controlli*. il metodo **fastForward** imposta il valore di **rate** su 5,0, mentre i *controlli*. la **frequenza** delle modifiche al metodo **fastReverse** è 5,0.

Non è possibile modificare la velocità di riproduzione di alcuni tipi di supporto. Usare le *Impostazioni*. **Metodo IsValid** per determinare se questa proprietà può essere specificata per un particolare elemento multimediale.

**Windows Media Player 10 Mobile**: questa proprietà accetta o restituisce solo i valori-5,0, 1,0 o 5,0.

## <a name="examples"></a>Esempio

Nell'esempio seguente viene creato un elemento HTML SELECT che consente all'utente di modificare la velocità di riproduzione del supporto corrente. Le opzioni di selezione offrono velocità di riproduzione normali, a metà velocità e a velocità doppia. L'oggetto **Player** è stato creato con ID = "Player".


```
<!-- Create the HTML SELECT element. -->
<SELECT  ID = pbRATE  NAME = "pbRATE"  LANGUAGE="JScript"
         onChange="
                   /* Test whether playback rate can be set. */
                   if(Player.settings.IsAvailable('Rate'))

                   /* Set the playback rate based on the current
                      value of the SELECT element. */
                   Player.settings.rate = this.value
">

/* Create the OPTION list. */
<OPTION VALUE = 1>NORMAL</OPTION>
<OPTION VALUE = .5>half speed</OPTION>
<OPTION VALUE = 2>2 speed</OPTION>
</SELECT>

```



## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|------------------------------------------------------------------------------------|
| Versione<br/> | Windows Media Player versione 7,0 o successiva.<br/>                              |
| DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Controls. fastForward**](controls-fastforward.md)
</dt> <dt>

[**Controls. fastReverse**](controls-fastreverse.md)
</dt> <dt>

[**Oggetto Settings**](settings-object.md)
</dt> <dt>

[**Settings. available**](settings-isavailable.md)
</dt> </dl>

 

 





