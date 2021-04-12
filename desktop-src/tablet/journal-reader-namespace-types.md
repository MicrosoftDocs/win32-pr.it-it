---
description: In questa sezione vengono documentati i tipi XML utilizzati dal componente Reader Journal.
ms.assetid: 08b45fe0-a505-4cc0-9791-764a87e8f1eb
title: Tipi di spazio dei nomi Reader Journal
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4c4e8e3d812eea879ca9dd31680aa2834d6dfe50
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104231908"
---
# <a name="journal-reader-namespace-types"></a>Tipi di spazio dei nomi Reader Journal

In questa sezione vengono documentati i tipi XML utilizzati dal componente Reader Journal.

## <a name="in-this-section"></a>Contenuto della sezione



| Tipo                                                                                  | Descrizione                                                                                                                                                                                                    |
|---------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**ComplexType AlternatesListType**](alternateslisttype-complex-type.md)             | Definisce il tipo che contiene l'elenco di alternative di riconoscimento per una parola di input penna.<br/>                                                                                                                  |
| [**ComplexType BackgroundImageType**](backgroundimagetype-complex-type.md)           | Definisce il tipo che include le informazioni sull'immagine di sfondo utilizzata dalla nota Journal, se presente.<br/>                                                                                                |
| [**ComplexType BackgroundType**](backgroundtype-complex-type.md)                     | Definisce il tipo che contiene le informazioni di base per la nota Journal.<br/>                                                                                                                     |
| [**ComplexType BaselineType**](baselinetype-complex-type.md)                         | Definisce il tipo che contiene informazioni sulla linea di base di un paragrafo.<br/>                                                                                                                       |
| [AttributeGroup BoundsType](boundstype-attributegroup.md)                            | Definisce un gruppo di attributi utilizzato da un'ampia gamma di elementi in un file journal XML.<br/>                                                                                                             |
| [**SimpleType ColorType**](colortype-simple-type.md)                                 | Definisce il tipo utilizzato per specificare i valori validi per il colore di determinati elementi in un file XML del journal.<br/>                                                                                      |
| [Gruppo ContentGroup](contentgroup-group.md)                                          | Definisce il tipo che contiene un set di contenuto raggruppato in una nota del journal.<br/>                                                                                                                          |
| [**ComplexType ContentType**](contenttype-complex-type.md)                           | Definisce il tipo che contiene una forma di contenuto all'interno di un file XML del journal.<br/>                                                                                                                      |
| [**SimpleType ContentTypeType**](contenttypetype-simple-type.md)                     | Definisce il tipo che definisce i valori validi per l'attributo **Type** dell' [elemento Content \[ Journal Reader \]](content-element--journal-reader.md).<br/>                                             |
| [**ComplexType DrawingType**](drawingtype-complex-type.md)                           | Definisce il tipo che contiene l'input penna che è stato classificato dal motore di analisi del Journal come [elemento di disegno](drawing-element.md) (in contrapposizione a un [elemento InkWord](inkword-element.md)).<br/>  |
| [**ComplexType FlagType**](flagtype-complex-type.md)                                 | Definisce il tipo che contiene l'immagine binaria codificata e le informazioni sulla posizione per un flag incorporato in un documento Journal.<br/>                                                                         |
| [**ComplexType GroupNodeType**](groupnodetype-complex-type.md)                       | Definisce il tipo che contiene un set di contenuto raggruppato in una nota del journal.<br/>                                                                                                                          |
| [**ComplexType HorizontalType**](horizontaltype-complex-type.md)                     | Definisce il tipo che contiene informazioni sulle linee orizzontali utilizzate dalla cancelleria in una nota Journal.<br/>                                                                                         |
| [**complexType ImageType**](imagetype-complex-type.md)                               | Definisce il tipo che contiene le informazioni binarie per un'immagine in una nota del journal. Vedere anche [**complexType BackgroundImageType**](backgroundimagetype-complex-type.md).<br/>                     |
| [**ComplexType InkWordType**](inkwordtype-complex-type.md)                           | Definisce il tipo che contiene i dati dell'input penna, le alternative e la confidenza per il contenuto di input penna che è un [elemento InkWord](inkword-element.md) (in contrapposizione a un [elemento Drawing](drawing-element.md)).<br/> |
| [**ComplexType JournalPageType**](journalpagetype-complex-type.md)                   | Definisce il tipo che contiene una singola pagina in una nota del journal.<br/>                                                                                                                                |
| [**ComplexType LineLayoutType**](linelayouttype-complex-type.md)                     | Definisce il tipo che contiene informazioni sulle righe utilizzate in una determinata cancelleria della nota Journal.<br/>                                                                                      |
| [**SimpleType LineLayoutStyleType**](linelayoutstyletype-simple-type.md)             | Definisce i valori validi per l'attributo di **stile** dell' [elemento LineLayout](linelayout-element.md).<br/>                                                                                           |
| [**ComplexType del tipo di elemento**](linetype-complex-type.md)                                 | Definisce il tipo che contiene una riga di paragrafo.<br/>                                                                                                                                                 |
| [**ComplexType MarginType**](margintype-complex-type.md)                             | Definisce il tipo che contiene i dettagli relativi ai margini nella nota Journal, ad esempio stile, colore e posizione.<br/>                                                                               |
| [**SimpleType MarginTypeType**](margintypetype-simple-type.md)                       | Definisce il tipo che contiene i valori validi per l'attributo del **tipo** per l' [elemento Margin](margin-element.md).<br/>                                                                                |
| [**ComplexType ParagraphType**](paragraphtype-complex-type.md)                       | Definisce il tipo che include un paragrafo in una nota del journal.<br/>                                                                                                                                          |
| [**ComplexType ParagraphLineMetricsType**](paragraphlinemetricstype-complex-type.md) | Definisce il tipo che contiene informazioni sulle metriche della riga di un paragrafo, ad esempio la baseline.<br/>                                                                                             |
| [**ComplexType ReflowType**](reflowtype-complex-type.md)                             | Definisce il tipo che indica che il gruppo è stato propagato.<br/>                                                                                                                                        |
| [**ComplexType ScalarTransformType**](scalartransformtype-complex-type.md)           | Definisce il tipo che include le informazioni su qualsiasi trasformazione applicata a input penna.<br/>                                                                                                                |
| [**ComplexType StationeryType**](stationerytype-complex-type.md)                     | Definisce il tipo che contiene la cancelleria utilizzata dalla nota Journal.<br/>                                                                                                                             |
| [**ComplexType TextType**](texttype-complex-type.md)                                 | Definisce il tipo che contiene il valore di testo in un [ \[ \] lettore Journal dell'elemento di contenuto](content-element--journal-reader.md).<br/>                                                                       |
| [**ComplexType TitleAreaType**](titleareatype-complex-type.md)                       | Definisce il tipo che contiene le informazioni sulla posizione e sui limiti del titolo in una nota del journal.<br/>                                                                                                     |
| [**ComplexType TitleInfoType**](titleinfotype-complex-type.md)                       | Definisce il tipo che contiene informazioni sul titolo in una nota del journal.<br/>                                                                                                                       |
| [**ComplexType TitleType**](titletype-complex-type.md)                               | Definisce il tipo che contiene le informazioni sul titolo per la nota Journal.<br/>                                                                                                                              |
| [**ComplexType VerticalType**](verticaltype-complex-type.md)                         | Definisce il tipo che contiene i dettagli sulle linee verticali utilizzate nella cancelleria di una nota del journal.<br/>                                                                                                |



 

 

 




