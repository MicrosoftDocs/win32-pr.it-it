---
description: ICE30 verifica che l'installazione dei componenti contenenti lo stesso file non installi mai il file più di una volta nella stessa directory.
ms.assetid: 74cb455b-a53e-4c6b-98ff-08cf0858f11f
title: ICE30
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3ba807ec1eb3bde54b1f115e93c531f24414b75e7a293c8ff1b7d7ff1d3abca8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119528661"
---
# <a name="ice30"></a>ICE30

ICE30 verifica che l'installazione dei componenti contenenti lo stesso file non installi mai il file più di una volta nella stessa directory.

ICE30 passa a ogni componente nella [tabella Component](component-table.md) e quindi determina la directory di destinazione del componente dalla [tabella Directory](directory-table.md). Verifica quindi quali di questi componenti vengono installati nella stessa directory di destinazione. Infine, usa la [tabella File](file-table.md) per verificare che nessuno dei file in questi componenti abbia lo stesso nome.

ICE30 controlla sia i nomi di file lunghi (LFN) che i nomi di file brevi (SFN).

ICE30 non valuta le proprietà nella risoluzione delle directory perché queste proprietà possono cambiare in fase di esecuzione e modificare lo schema di risoluzione della directory. Ciò significa che ICE30 è in grado di rilevare conflitti di file dovuti a directory con la stessa proprietà nei percorsi, ma non rileva conflitti risultanti da due proprietà con lo stesso valore.

## <a name="result"></a>Risultato

ICE30 pubblica un messaggio di errore per ogni coppia di componenti che installa lo stesso file nella stessa directory.

## <a name="example"></a>Esempio

Nell'esempio illustrato vengono restituiti due volte tutti gli errori seguenti.



| Errore o avviso ICE30                                                                                                                                                                                                                                                                    | Descrizione                                                                                                                                                                                                                                                                                                                                                                                                                                    |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| ERRORE: il file di destinazione 'README.1st' è installato in 'TARGETDIR PRODUCT' da due componenti diversi in un sistema \\ SFN: 'Component1' e 'Component2'. Questo interrompe il conteggio dei riferimenti ai componenti.                                                                                           | Component1 e Component2 hanno entrambi un file denominato "READEME.1st". Quando si usano nomi di file brevi, il programma di installazione installa sia Dir1 che Dir2 nella stessa directory, TARGETDIR \\ PRODUCT.<br/> ICE30 genera due errori, uno per ogni file. In un ambiente di creazione che visualizza i percorsi degli errori, il primo errore si trova in corrispondenza di una voce di un file nella tabella [file](file-table.md)e il secondo nella posizione dell'altro file.<br/> |
| ERRORE: l'installazione di un componente condizionale causerebbe l'installazione del file di destinazione 'README.1st' in 'TARGETDIR COMMON TOOLS' da parte di due componenti diversi in un sistema \\ LFN: 'Component3' e 'Component4'. In questo modo si interrompe il conteggio dei riferimenti ai componenti.                      | Component4 include una voce nella colonna Condizione della [tabella Component](component-table.md) e Component3 no. Se [**VersionNT**](versionnt.md) è True, Component4 viene installato e si verifica un conflitto con il file Leggimi.1 sempre installato da Component3.<br/> ICE30 genera 4 errori, una coppia per SFN e una per LFN.<br/>                                                                                            |
| AVVISO: il file di destinazione 'README.1st' potrebbe essere installato in 'TARGETDIR COMMON TOOLS' da due diversi componenti condizionali in un sistema \\ SFN: 'Component4' e 'Component5'. Se le condizioni non si escludono a vicenda, ciò interromperà il sistema di conteggio dei riferimenti ai componenti. | Poiché Component4 e Component5 hanno entrambe voci nella colonna Condizione della tabella [Componente,](component-table.md) questo conflitto di file potrebbe non verificarsi. ICE30 invia un avviso solo perché le condizioni devono essere determinate al momento dell'installazione.<br/> ICE30 genera 4 avvisi, una coppia per SFN e una per LFN.<br/>                                                                                            |



 

[Tabella dei componenti](component-table.md) (parziale)



| Componente  | Directory | Condition |
|------------|-----------|-----------|
| Componente1 | Dir1      |           |
| Componente2 | Dir2      |           |
| Componente3 | Dir3      |           |
| Componente4 | Dir3      | VersionNT |
| Componente5 | Dir3      | Versione9X |



 

[Tabella directory](directory-table.md)



| Directory | Directory \_ padre | DefaultDir                    |
|-----------|-------------------|-------------------------------|
| SOURCEDIR |                   | Targetdir                     |
| Dir1      | SOURCEDIR         | Product \| Component1 Product:. |
| Dir2      | SOURCEDIR         | Prodotto:.                     |
| Dir3      | SOURCEDIR         | Strumenti \| comuni:         |



 

[Tabella file](file-table.md) (parziale)



| File  | Componente\_ | FileName   |
|-------|-------------|------------|
| File1 | Componente1  | README.1st |
| File2 | Componente2  | README.1st |
| File3 | Componente3  | README.1st |
| File4 | Componente4  | README.1st |
| File5 | Componente5  | README.1st |



 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Informazioni di riferimento su ICE](ice-reference.md)
</dt> </dl>

 

 




