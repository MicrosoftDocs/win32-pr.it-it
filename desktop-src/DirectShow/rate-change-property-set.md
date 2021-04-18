---
description: Il set di proprietà rate Change Abilita i filtri di origine/parser MPEG-2 per modificare la velocità di riproduzione. I decodificatori MPEG-2 devono supportare questo set di proprietà. Il navigatore DVD e il motore di buffer del flusso utilizzano entrambi questa proprietà impostata per controllare le frequenze di riproduzione.
ms.assetid: f88c64ce-af76-49fe-8ebd-029928506243
title: Set di proprietà rate Change (dvdmedia. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e56b679b0ce9b0127b15c69cd02b016a4990b6f2
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106328072"
---
# <a name="rate-change-property-set"></a>Set di proprietà di modifica della frequenza

Il set di proprietà rate Change Abilita i filtri di origine/parser MPEG-2 per modificare la velocità di riproduzione. I decodificatori MPEG-2 devono supportare questo set di proprietà. Il navigatore DVD e il motore di buffer del flusso utilizzano entrambi questa proprietà impostata per controllare le frequenze di riproduzione.



|                   |                               |
|-------------------|-------------------------------|
| GUID set di proprietà | \_TSRateChange KSPROPSETID \_ |



 



| ID proprietà                                                                   | Descrizione                                                                            |
|-------------------------------------------------------------------------------|----------------------------------------------------------------------------------------|
| [**\_Correttivi della velocità am \_**](am-rate-correctts-property.md)                     | Informa il decodificatore che lo strumento di spostamento sta impostando i timestamp corretti.             |
| \_Frequenza \_ ExactRateChange                                                     | Obsoleta.                                                                              |
| [**\_Frequenza \_ MaxFullDataRate**](am-rate-maxfulldatarate-property.md)         | Esegue una query sul decodificatore per la velocità massima dei dati del decodificatore.                               |
| [**\_Frequenza \_ QueryFullFrameRate**](am-rate-queryfullframerate-property.md)   | Esegue una query sul decodificatore per la frequenza massima dei fotogrammi del decodificatore.                         |
| [**\_Frequenza \_ QueryLastRateSegPTS**](am-rate-querylastratesegpts-property.md) | Esegue una query sul decodificatore per l'ora di inizio del segmento di frequenza impostato più di recente. |
| [**\_Frequenza \_ SimpleRateChange**](am-rate-simpleratechange-property.md)       | Invia una modifica di velocità al decodificatore.                                                    |
| \_Passaggio velocità \_ am                                                                | Obsoleta. Vedere [set di proprietà di avanzamento frame](frame-stepping-property-set.md).          |
| [**\_Frequenza \_ UseRateVersion**](am-rate-userateversion-property.md)           | Specifica la versione del meccanismo di modifica della frequenza da usare.                           |



 

## <a name="remarks"></a>Commenti

Nel contesto di questo set di proprietà, rate misura la frequenza con cui i timestamp avanzano rispetto all'orologio di riferimento. Valuta l'inverso della velocità di riproduzione. Se ad esempio la velocità di riproduzione è 2x, è necessario che i timestamp aumentino a 1/2 della normale frequenza. Questo si traduce in una velocità di riproduzione più veloce, perché il rendering degli esempi è precedente al normale.

Gli esempi vengono inviati al decodificatore con un timestamp uguale all'ora di presentazione a una velocità di 1x. Il decodificatore deve ridimensionare i timestamp degli esempi di output in base all'ora di presentazione corretta per la tariffa corrente. Se, ad esempio, la frequenza è 1/2 (ovvero la velocità di riproduzione è 2x), il decodificatore deve ridimensionare i timestamp di 1/2. In genere, solo I frame I hanno timestamp. Il decodificatore deve interpolare i timestamp per i frame B e P. Si noti che durante la riproduzione inversa, i timestamp continuano ad aumentare: i timestamp non passano mai indietro.

Sono definite due versioni del set di proprietà rate Change, ovvero la versione 1,0 e la versione 1,1. Il comportamento predefinito è fornito dalla versione 1,0. I fornitori di decodificatori sono invitati a supportare la versione 1,1, perché offre un'esperienza di riproduzione più fluida. Il navigatore DVD usa attualmente la versione 1,0. Il motore buffer del flusso usa la versione 1,1.

### <a name="rate-change-version-10"></a>Modifica della frequenza versione 1,0

La versione 1,0 del set di proprietà rate Change definisce il comportamento predefinito per i decodificatori MPEG-2.

Il filtro di origine segnala una modifica della frequenza impostando la proprietà [**am \_ rate \_ SimpleRateChange**](am-rate-simpleratechange-property.md) . I dati per questa proprietà sono la nuova velocità, più l'ora di inizio sull'esempio di input quando la velocità viene applicata. Il decodificatore mantiene una coda di modifiche di frequenza in sospeso, ordinate in base all'ora di inizio.

Prima che il navigatore DVD cambi a una velocità non 1x, recapita tutti gli esempi in sospeso, imposta temporaneamente la velocità su 1,0 e Scarica il grafo. Imposta quindi la nuova velocità. Tutte le modifiche di frequenza sono pianificate per la fine del VOBU corrente (unità oggetto video). Si noti che lo svuotamento del grafico Reimposta l'ora di presentazione su zero.

Il navigatore DVD funziona in modalità *Smooth* o in *modalità di analisi*. In modalità Smooth, invia ogni frame al decodificatore, inclusi i fotogrammi B e i fotogrammi P. Il navigatore DVD usa la modalità Smooth ogni volta che la velocità di riproduzione è maggiore di zero ma minore della velocità dati superati del decodificatore. Se la velocità di riproduzione è minore di zero (riproduzione inversa) o supera la velocità massima di dati del decodificatore, il navigatore DVD usa la modalità di analisi, in cui invia solo i frame i al decodificatore. A velocità molto elevate, potrebbe ignorare alcuni frame I; ad esempio, può inviare tutti gli altri frame I.

Per impostazione predefinita, il navigatore DVD disattiva il flusso audio per le tariffe diverse da 1,0. È possibile modificare questa impostazione chiamando [**IDVDControl2:: SetOption**](/windows/desktop/api/Strmif/nf-strmif-idvdcontrol2-setoption) con il \_ flag AudioDuringFFwdRew di DVD.

### <a name="rate-change-version-11"></a>Modifica della frequenza versione 1,1

La versione 1,1 del set di proprietà rate Change segue gli stessi principi di base della versione 1,0, con le differenze seguenti:

-   Il filtro di origine segnala al decodificatore di usare la versione 1,1 impostando la proprietà [**am \_ rate \_ UseRateVersion**](am-rate-userateversion-property.md) . In caso contrario, il decodificatore deve usare il comportamento della versione 1,0.
-   Il filtro di origine non Scarica il grafico tra le variazioni di frequenza. I timestamp aumentano quindi in modo monotonico tra i limiti di modifica della frequenza, anziché reimpostarli su zero.
-   Anziché accodare una modifica di frequenza per una particolare ora di riferimento, il filtro di origine può specificare che una modifica della frequenza si applica all' *esempio più avanzato* del decodificatore, definito come esempio all'inizio della coda in uscita del decodificatore. A tale scopo, il filtro di origine usa la proprietà [**am \_ rate \_ SimpleRateChange**](am-rate-simpleratechange-property.md) , ma imposta l'ora di inizio uguale a-1.
-   Il filtro di origine può eseguire una query sul decodificatore per l'ora di inizio della modifica della frequenza accodata più di recente. Per questo scopo, usa la proprietà [**am \_ rate \_ QueryLastRateSegPTS**](am-rate-querylastratesegpts-property.md) .
-   Il filtro di origine non elimina gli esempi. Se la frequenza supera la velocità massima dei dati del decodificatore, il decodificatore deve rilasciare i frame in base alle esigenze.
-   Il filtro di origine non disattiva il flusso audio, indipendentemente dalla velocità massima dei dati del decodificatore audio. Il decodificatore audio può eliminare campioni se la velocità di riproduzione supera la frequenza massima del decodificatore. Tuttavia, deve comunque mantenere la coda delle modifiche della frequenza pianificata.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------|---------------------------------------------------------------------------------------|
| Intestazione<br/> | <dl> <dt>Dvdmedia. h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Set di proprietà](property-sets.md)
</dt> </dl>

 

 




