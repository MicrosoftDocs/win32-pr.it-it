---
title: Impostazioni.rate
description: La proprietà rate specifica o recupera la frequenza di riproduzione corrente dei contenuti multimediali video.
ms.assetid: 0f95f7ac-1bb6-4c80-89eb-eb300a03a0f1
keywords:
- Impostazioni.rate Windows Media Player
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
ms.openlocfilehash: 01936462593b8b27a8d45f2e3e4090b9cf242d79e1d9b1c2cda00c152bd41182
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119646401"
---
# <a name="settingsrate"></a>Impostazioni.rate

La **proprietà rate** specifica o recupera la frequenza di riproduzione corrente dei contenuti multimediali video.

## <a name="syntax"></a>Sintassi

player.settings.rate

## <a name="possible-values"></a>Valori possibili

Questa proprietà è un numero **di** lettura/scrittura (**double**) con valore predefinito 1.0.

## <a name="remarks"></a>Commenti

Questa proprietà funge da valore moltiplicatore che consente di riprodurre un clip a una velocità più veloce o più lenta. Il valore predefinito 1.0 indica la velocità di creazione. Si noti che una traccia audio diventa difficile da comprendere a velocità inferiori a 0,5 o superiori a 1,5. Una velocità di riproduzione di 2 equivale al doppio della velocità di riproduzione normale.

Windows Media Player tenterà di usare il più efficace di quattro diverse modalità di riproduzione. Queste modalità sono la riproduzione video uniforme con audio intonazione mantenuta, la riproduzione video uniforme con il tono audio non mantenuto, la riproduzione video uniforme senza audio e la riproduzione video con fotogrammi chiave senza audio. La modalità scelta dal Lettore dipende da numerosi fattori, tra cui il tipo di file e la posizione, il sistema operativo, la rete e il server.

Si applicano anche altre considerazioni, a seconda del tipo di supporto:

-   Windows File WMV (Media Format) e ASF: i valori ottimali per questa proprietà sono da 1 a 10 o da 1 a 10 per la riproduzione inversa. Anche i valori da 0.5 a 1.0 o da -0.5 a -1.0 possono funzionare correttamente nei casi in cui è possibile mantenere l'audio pitch, ad esempio durante la riproduzione di file che si trovano nel computer locale. I valori con una grandezza assoluta maggiore di 10 sono consentiti, ma non sono molto significativi.
-   Altri tipi di supporti video: questa proprietà può variare da 0 a 9. I valori negativi non sono consentiti. I valori minori di 1 rappresentano il movimento lento. I valori superiori a 9 sono consentiti, ma non sono molto significativi.

Controlli . **Il metodo fastForward** modifica il valore **della frequenza** in 5,0, mentre *il controllo .* **Il metodo fastReverse** cambia **la frequenza** a 5.0.

Non è possibile modificare la velocità di riproduzione di alcuni tipi di supporti. Usare il *Impostazioni*. **Metodo isAvailable** per determinare se questa proprietà può essere specificata per un particolare elemento multimediale.

**Windows Media Player 10 Mobile:** questa proprietà accetta o restituisce solo valori -5.0, 1.0 o 5.0.

## <a name="examples"></a>Esempio

Nell'esempio seguente viene creato un elemento HTML SELECT che consente all'utente di modificare la velocità di riproduzione del supporto corrente. Le opzioni SELECT offrono velocità normale, velocità media e velocità di riproduzione a doppia velocità. **L'oggetto** Player è stato creato con ID = "Player".


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
| Versione<br/> | Windows Media Player versione 7.0 o successiva.<br/>                              |
| DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Controls.fastForward**](controls-fastforward.md)
</dt> <dt>

[**Controls.fastReverse**](controls-fastreverse.md)
</dt> <dt>

[**Impostazioni Oggetto**](settings-object.md)
</dt> <dt>

[**Impostazioni.isAvailable**](settings-isavailable.md)
</dt> </dl>

 

 





