---
description: Il set di proprietà Rate Change consente ai filtri di origine/parser MPEG-2 di modificare la velocità di riproduzione. I decodificatori MPEG-2 devono supportare questo set di proprietà. Lo strumento di navigazione DVD e il motore di buffer di flusso usano entrambi questa proprietà impostata per controllare le velocità di riproduzione.
ms.assetid: f88c64ce-af76-49fe-8ebd-029928506243
title: Impostare le proprietà Rate Change (Dvdmedia.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5299b744869a4c9a12b50a9e738104999aab5dcd19a800fc0ac3ddb3717e8617
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119747411"
---
# <a name="rate-change-property-set"></a>Impostare la proprietà Rate Change

Il set di proprietà Rate Change consente ai filtri di origine/parser MPEG-2 di modificare la velocità di riproduzione. I decodificatori MPEG-2 devono supportare questo set di proprietà. Lo strumento di navigazione DVD e il motore di buffer di flusso usano entrambi questa proprietà impostata per controllare le velocità di riproduzione.



| Etichetta | Valore |
|-------------------|-------------------------------|
| GUID set di proprietà | AM \_ KSPROPSETID \_ TSRateChange |



 



| ID proprietà                                                                   | Descrizione                                                                            |
|-------------------------------------------------------------------------------|----------------------------------------------------------------------------------------|
| [**AM \_ RATE \_ CorrectTS**](am-rate-correctts-property.md)                     | Informa il decodificatore che lo strumento di navigazione sta impostando i timestamp corretti.             |
| AM \_ RATE \_ ExactRateChange                                                     | Obsoleta.                                                                              |
| [**AM \_ RATE \_ MaxFullDataRate**](am-rate-maxfulldatarate-property.md)         | Esegue una query sul decodificatore per la velocità massima dei dati del decodificatore.                               |
| [**AM \_ RATE \_ QueryFullFrameRate**](am-rate-queryfullframerate-property.md)   | Esegue una query sul decodificatore per la frequenza massima di fotogrammi completi del decodificatore.                         |
| [**AM \_ RATE \_ QueryLastRateSegPTS**](am-rate-querylastratesegpts-property.md) | Esegue una query sul decodificatore per l'ora di inizio del segmento di frequenza impostato più di recente. |
| [**AM \_ RATE \_ SimpleRateChange**](am-rate-simpleratechange-property.md)       | Invia una modifica della frequenza al decodificatore.                                                    |
| Passaggio AM \_ RATE \_                                                                | Obsoleta. Vedere [Frame Stepping Property Set](frame-stepping-property-set.md).          |
| [**AM \_ RATE \_ UseRateVersion**](am-rate-userateversion-property.md)           | Specifica la versione del meccanismo di modifica della frequenza da usare.                           |



 

## <a name="remarks"></a>Commenti

Nel contesto di questo set di proprietà, rate misura la velocità di avanzamento dei timestamp rispetto all'orologio di riferimento. Valutare l'inverso della velocità di riproduzione. Ad esempio, se la velocità di riproduzione è 2 volte, i timestamp devono aumentare a 1/2 la velocità normale. Ciò si traduce in una velocità di riproduzione più veloce, perché il rendering dei campioni viene eseguito prima del normale.

I campioni vengono inviati al decodificatore con un timestamp uguale all'ora di presentazione a una velocità di 1x. Il decodificatore deve ridimensionare i timestamp degli esempi di output in base all'ora di presentazione corretta per la frequenza corrente. Ad esempio, se la velocità è 1/2 (ovvero la velocità di riproduzione è 2 volte), il decodificatore deve ridimensionare i timestamp di 1/2. In genere, solo I fotogrammi hanno timestamp. Il decodificatore deve interpolare i timestamp per i fotogrammi B e P. Si noti che durante la riproduzione inversa, i timestamp continuano ad aumentare, in modo che i timestamp non vadano mai indietro.

Sono definite due versioni del set di proprietà Rate Change, la versione 1.0 e la versione 1.1. Il comportamento predefinito è dato dalla versione 1.0. I fornitori di decodificatori sono invitati a supportare la versione 1.1, perché offre un'esperienza di riproduzione più fluida. Dvd Navigator usa attualmente la versione 1.0. Il motore di buffer di flusso usa la versione 1.1.

### <a name="rate-change-version-10"></a>Modifica della frequenza versione 1.0

La versione 1.0 del set di proprietà Rate Change definisce il comportamento predefinito per i decodificatori MPEG-2.

Il filtro di origine segnala una modifica della frequenza impostando la [**proprietà AM \_ RATE \_ SimpleRateChange.**](am-rate-simpleratechange-property.md) I dati per questa proprietà sono la nuova frequenza e l'ora di inizio del campione di input quando la frequenza ha effetto. Il decodificatore gestisce una coda di modifiche della frequenza in sospeso, ordinate in base all'ora di inizio.

Prima che lo strumento di spostamento DVD cambi a una velocità non 1x, recapita tutti i campioni in sospeso, imposta temporaneamente la velocità su 1.0 e scarica il grafico. Imposta quindi la nuova frequenza. Tutte le modifiche alla frequenza sono pianificate per la fine del VOBU corrente (unità oggetto video). Si noti che lo scaricamento del grafo reimposta l'ora di presentazione su zero.

Lo strumento di navigazione DVD opera in *modalità uniforme o* in modalità di *analisi.* In modalità smooth, invia ogni fotogramma al decodificatore, inclusi i fotogrammi B e P. Lo strumento di navigazione DVD usa la modalità smooth ogni volta che la velocità di riproduzione è maggiore di zero, ma minore della velocità dei dati maxmimum del decodificatore. Se la velocità di riproduzione è minore di zero (riproduzione inversa) o supera la velocità dati massima del decodificatore, lo strumento di navigazione DVD usa la modalità di analisi, in cui invia solo i fotogrammi I al decodificatore. A velocità molto elevate, può ignorare alcuni fotogrammi I; ad esempio, può inviare ogni altro frame I.

Per impostazione predefinita, lo strumento di spostamento DVD disattiva il flusso audio per frequenze diverse da 1.0. È possibile modificare questa impostazione chiamando [**IDvdControl2::SetOption**](/windows/desktop/api/Strmif/nf-strmif-idvdcontrol2-setoption) con il \_ flag DVD AudioDuringFFfwdRew.

### <a name="rate-change-version-11"></a>Modifica della frequenza versione 1.1

La versione 1.1 del set di proprietà Rate Change segue gli stessi principi di base della versione 1.0, con le differenze seguenti:

-   Il filtro di origine segnala al decodificatore di usare la versione 1.1 impostando la [**proprietà \_ AM RATE \_ UseRateVersion.**](am-rate-userateversion-property.md) In caso contrario, il decodificatore deve usare il comportamento della versione 1.0.
-   Il filtro di origine non scarica il grafico tra le modifiche della frequenza. I timestamp aumentano quindi in modo monotono attraverso i limiti di modifica della frequenza, anziché reimpostarsi su zero.
-   Anziché eseguire l'accodamento di una modifica della frequenza per un determinato tempo di riferimento, il filtro di origine può specificare che una modifica della frequenza si applica al campione più avanti del decodificatore, definito come campione nella parte superiore della coda in uscita del decodificatore. A tale scopo, il filtro di origine usa la [**proprietà AM \_ RATE \_ SimpleRateChange,**](am-rate-simpleratechange-property.md) ma imposta l'ora di inizio su -1.
-   Il filtro di origine può eseguire una query sul decodificatore per l'ora di inizio della modifica della frequenza accodata più di recente. A questo scopo usa [**la proprietà AM RATE \_ \_ QueryLastRateSegPTS.**](am-rate-querylastratesegpts-property.md)
-   Il filtro di origine non elimina gli esempi. Se la velocità supera la velocità massima dei dati del decodificatore, il decodificatore deve eliminare i fotogrammi in base alle esigenze.
-   Il filtro di origine non disattiva il flusso audio, indipendentemente dalla velocità massima dei dati del decodificatore audio. Il decodificatore audio può eliminare i campioni se la velocità di riproduzione supera la velocità massima del decodificatore. Tuttavia, deve comunque mantenere la coda delle modifiche pianificate alla frequenza.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------|---------------------------------------------------------------------------------------|
| Intestazione<br/> | <dl> <dt>Dvdmedia.h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Set di proprietà](property-sets.md)
</dt> </dl>

 

 




