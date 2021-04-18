---
description: ICE30 verifica che l'installazione dei componenti contenenti lo stesso file non installi mai il file più di una volta nella stessa directory.
ms.assetid: 74cb455b-a53e-4c6b-98ff-08cf0858f11f
title: ICE30
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 78fa96899231015d864e5a0912b8ff73cedbbe75
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106314225"
---
# <a name="ice30"></a>ICE30

ICE30 verifica che l'installazione dei componenti contenenti lo stesso file non installi mai il file più di una volta nella stessa directory.

ICE30 passa a tutti i componenti della [tabella dei componenti](component-table.md) e quindi determina la directory di destinazione del componente dalla [tabella di directory](directory-table.md). Verifica quindi quale di questi componenti viene installato nella stessa directory di destinazione. Infine, utilizza la [tabella file](file-table.md) per verificare che nessuno dei file presenti in questi componenti abbia lo stesso nome.

ICE30 controlla i nomi di file lunghi (LFN) e i nomi di file brevi (SFN).

ICE30 non valuta le proprietà nella risoluzione delle directory perché queste proprietà possono cambiare in fase di esecuzione e modificare lo schema di risoluzione della directory. Ciò significa che ICE30 è in grado di rilevare conflitti di file a causa di directory con la stessa proprietà nei percorsi, ma non rileva conflitti che risultano da due proprietà con lo stesso valore.

## <a name="result"></a>Risultato

ICE30 Invia un messaggio di errore per ogni coppia di componenti che installa lo stesso file nella stessa directory.

## <a name="example"></a>Esempio

L'esempio illustrato restituisce due volte gli errori seguenti.



| Errore o avviso ICE30                                                                                                                                                                                                                                                                    | Descrizione                                                                                                                                                                                                                                                                                                                                                                                                                                    |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| ERRORE: il file di destinazione ' README. 1st ' è installato in ' TARGETDIR \\ Product ' da due componenti diversi in un sistema SFN:' Component1' è Component2'. Il conteggio dei riferimenti del componente viene interrotto.                                                                                           | Component1 e Component2 hanno entrambi un file denominato "reademe. 1st". Quando si usano nomi di file brevi, il programma di installazione installa sia dir1 che dir2 nella stessa directory, TARGETDIR \\ Product.<br/> ICE30 generano due errori, uno per ogni file. In un ambiente di creazione che Visualizza i percorsi degli errori, il primo errore si trova nella voce di un file nella [tabella file](file-table.md)e il secondo nella posizione dell'altro file.<br/> |
| ERRORE: l'installazione di un componente condizionale comporterebbe l'installazione del file di destinazione ' README. 1st ' in ' TARGETDIR \\ Common Tools ' da due componenti diversi in un sistema LFN:' Component3' è Component4'. In questo modo si interrompe il conteggio dei riferimenti ai componenti.                      | Component4 include una voce nella colonna Condition della [tabella Component](component-table.md) e Component3 No. Se [**VersionNT**](versionnt.md) è true, Component4 è installato e si verifica un conflitto con il file Leggimi. 1 sempre installato da Component3.<br/> ICE30 genera 4 errori, una coppia per SFN, uno per LFN.<br/>                                                                                            |
| AVVISO: il file di destinazione ' README. 1st ' potrebbe essere installato in ' TARGETDIR \\ Common Tools ' da due diversi componenti condizionali in un sistema SFN:' Component4' è Component5'. Se le condizioni non si escludono a vicenda, il sistema di conteggio dei riferimenti ai componenti verrà interrotta. | Poiché Component4 e Component5 contengono entrambe voci nella colonna condizione della tabella dei [componenti](component-table.md) , questo conflitto di file potrebbe non verificarsi. ICE30 Invia un avviso solo perché le condizioni devono essere determinate al momento dell'installazione.<br/> ICE30 genera 4 avvisi, una coppia per SFN, uno per LFN.<br/>                                                                                            |



 

[Tabella componenti](component-table.md) (parziale)



| Componente  | Directory | Condizione |
|------------|-----------|-----------|
| Component1 | Dir1      |           |
| Component2 | Dir2      |           |
| Component3 | Dir3      |           |
| Component4 | Dir3      | VersionNT |
| Component5 | Dir3      | Version9X |



 

[Tabella directory](directory-table.md)



| Directory | \_Directory padre | DefaultDir                    |
|-----------|-------------------|-------------------------------|
| SOURCEDIR |                   | TARGETDIR                     |
| Dir1      | SOURCEDIR         | Prodotto \| Component1 prodotto:. |
| Dir2      | SOURCEDIR         | Prodotto:.                     |
| Dir3      | SOURCEDIR         | \|Strumenti comuni comuni:         |



 

[Tabella file](file-table.md) (parziale)



| File  | Componente\_ | FileName   |
|-------|-------------|------------|
| File1 | Component1  | FILE Leggimi. 1st |
| File2 | Component2  | FILE Leggimi. 1st |
| File3 | Component3  | FILE Leggimi. 1st |
| File4 | Component4  | FILE Leggimi. 1st |
| File5 | Component5  | FILE Leggimi. 1st |



 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Riferimento ghiaccio](ice-reference.md)
</dt> </dl>

 

 




