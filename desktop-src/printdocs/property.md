---
description: Informazioni sull'elemento Property nei documenti e nella stampa. Questo argomento non è corrente. Per le informazioni più aggiornate, vedere Specifica dello schema di stampa.
ms.assetid: 14631336-adfc-4edf-81ef-63e426d41c87
title: Proprietà (documenti e stampa)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dedeb635ec0f16fe4caee48d8e5db7fbcc8bfe6651e3bdc4de2166dbbc053286
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119886321"
---
# <a name="property-documents-and-printing"></a>Proprietà (documenti e stampa)

Questo argomento non è corrente. Per le informazioni più aggiornate, vedere Specifica [dello schema di stampa](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).

Un elemento Property dichiara un dispositivo, una formattazione del processo o un'altra proprietà pertinente il cui nome viene assegnato dal relativo attributo name. Un elemento Value viene usato per assegnare un valore alla proprietà .

Una proprietà può essere complessa, possibilmente contenente più sottoproprietà. Le sottoproprietà sono rappresentate anche da elementi Property.

## <a name="element-tag"></a>Tag di elemento

<Property>

## <a name="xml-attributes"></a>Attributi XML

Nella tabella seguente sono elencati gli attributi XML che possono essere relativi a questo elemento.



| Attributo XML   | Dettagli                                                                                                                    |
|-----------------|----------------------------------------------------------------------------------------------------------------------------|
| name<br/> | Contiene l'attributo name della proprietà , che è una proprietà standard o una proprietà definita privatamente. <br/> |



 

Per altre informazioni, vedere la [sezione Attributi XML.](xml-attributes.md)

## <a name="element-information"></a>Informazioni sull'elemento

Nella tabella seguente sono elencati gli elementi che possono essere elementi padre di questo elemento, gli elementi che possono essere elementi figlio di questo elemento ed eventuali restrizioni sull'elemento stesso.



| Category                   | Dettagli                                                                                                                                                                                                                                                                                                                      |
|----------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Elementi padre<br/> | PrintCapabilities <br/> Funzionalità<br/> PrintTicket<br/> Opzione<br/> ParameterDef<br/> Proprietà<br/> ScoredProperty<br/>                                                                                                                                                              |
| Elementi figlio<br/>  | Il sistema non assegna alcun significato all'ordinamento degli elementi. Se i client scelgono di attribuire un significato nell'ordinamento degli elementi, sono liberi di farlo. <br/> *Proprietà* (uno o più) *Valore* (zero o più)<br/> oppure <br/> *Proprietà* (zero o più) *Valore* (uno o più)<br/> |
| Questo elemento<br/>    | Non sono consentiti dati di tipo carattere.<br/> Sono consentiti elementi Value figlio duplicati di pari livello.<br/>                                                                                                                                                                                                        |



 

## <a name="configuration-dependencies"></a>Dipendenze di configurazione

Una proprietà può avere dipendenze di configurazione, tranne quando viene visualizzata all'interno di un elemento ParameterDef.

## <a name="element-usage"></a>Utilizzo degli elementi

Oltre a essere presenti negli elementi Feature e Option, gli elementi Property possono essere visualizzati al livello radice delle rispettive tecnologie sottostanti. Lo schema di stampa definisce un set di elementi Property che possono essere usati per descrivere un dispositivo in modo portabile. Tuttavia, se queste proprietà non sono sufficienti alle proprie esigenze come provider PrintCapabilities (in genere perché il dispositivo supportato presenta aspetti nuovi non previsti dallo schema di stampa), è possibile introdurre elementi Property privati. È possibile migliorare o elaborare le informazioni fornite da una proprietà pubblica aggiungendo una o più sottoproprietà private come contenuto dell'elemento della proprietà pubblica.

Gli elementi proprietà vengono definiti usando un tag di elemento XML, <Property> . A ogni proprietà viene assegnato un nome tramite il relativo attributo name. Il nome deve essere un QName XML e deve essere conforme alla convenzione dello spazio dei nomi. Per informazioni dettagliate, vedere [Attributi XML](xml-attributes.md). L'attributo Nome proprietà e la relativa posizione all'interno della gerarchia degli elementi Property padre (se si tratta di una sottoproprietà) identificano in modo univoco la proprietà all'interno del documento PrintCapabilities o PrintTicket.

Una proprietà può contenere uno o più elementi Value oppure uno o più elementi Property figlio (denominati sottoproprietà) o una combinazione di entrambi. Le sottoproprietà sono utili quando la proprietà stessa è costituita da più componenti. Ad esempio, una proprietà "ConsumableColor" potrebbe avere componenti "C", "M" e "Y".

## <a name="example"></a>Esempio

``` syntax
<psf:Property name="psk:DisplayName">
  <psf:Value xsi:type="xs:string">6</psf:Value>
</psf:Property>
```

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Specifica dello schema di stampa](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




