---
description: Questo argomento non è aggiornato. Per informazioni aggiornate, vedere la specifica dello schema di stampa.
ms.assetid: 14631336-adfc-4edf-81ef-63e426d41c87
title: Proprietà (documenti e stampa)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c9fb4a057b2cf7795262b595c59f9da0343fdf12
ms.sourcegitcommit: de72a1294df274b0a71dc0fdc42d757e5f6df0f3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/05/2021
ms.locfileid: "104351866"
---
# <a name="property-documents-and-printing"></a>Proprietà (documenti e stampa)

Questo argomento non è aggiornato. Per informazioni aggiornate, vedere la [specifica dello schema di stampa](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).

Un elemento Property dichiara un dispositivo, una formattazione del processo o un'altra proprietà pertinente il cui nome è fornito dall'attributo Name. Un elemento value viene usato per assegnare un valore alla proprietà.

Una proprietà può essere complessa, possibilmente contenente più sottoproprietà. Le sottoproprietà sono rappresentate anche dagli elementi della proprietà.

## <a name="element-tag"></a>Tag elemento

<Property>

## <a name="xml-attributes"></a>Attributi XML

Nella tabella seguente sono elencati gli attributi XML che possono essere relativi a questo elemento.



| Attributo XML   | Dettagli                                                                                                                    |
|-----------------|----------------------------------------------------------------------------------------------------------------------------|
| name<br/> | Include l'attributo Name della proprietà, che può essere una proprietà standard o una proprietà definita privatamente. <br/> |



 

Per ulteriori informazioni, vedere la sezione [attributi XML](xml-attributes.md) .

## <a name="element-information"></a>Informazioni sull'elemento

Nella tabella seguente sono elencati gli elementi che possono essere elementi padre di questo elemento, gli elementi che possono essere elementi figlio di questo elemento e tutte le restrizioni relative all'elemento stesso.



| Category                   | Dettagli                                                                                                                                                                                                                                                                                                                      |
|----------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Elementi padre<br/> | PrintCapabilities <br/> Funzionalità<br/> PrintTicket<br/> Opzione<br/> ParameterDef<br/> Proprietà<br/> ScoredProperty<br/>                                                                                                                                                              |
| Elementi figlio<br/>  | Il sistema non assegna alcun significato all'ordine degli elementi. Se i client scelgono di attribuire una certa importanza nell'ordinamento degli elementi, è possibile farlo liberamente. <br/> *Proprietà* (uno o più) *valore* (zero o più)<br/> oppure <br/> *Valore* *Property* (zero o più) (uno o più)<br/> |
| Questo elemento<br/>    | Non sono consentiti dati di tipo carattere.<br/> Sono consentiti elementi figlio duplicati di pari livello.<br/>                                                                                                                                                                                                        |



 

## <a name="configuration-dependencies"></a>Dipendenze di configurazione

Una proprietà può avere dipendenze di configurazione, tranne quando viene visualizzata all'interno di un elemento ParameterDef.

## <a name="element-usage"></a>Utilizzo elementi

Oltre a essere visualizzati all'interno degli elementi Feature e Option, gli elementi Property possono essere visualizzati a livello di radice delle rispettive tecnologie sottostanti. Lo schema di stampa definisce un set di elementi proprietà che possono essere usati per descrivere un dispositivo in modo portatile. Tuttavia, se queste proprietà non sono sufficienti per le proprie esigenze come provider PrintCapabilities, in genere perché il dispositivo supportato presenta aspetti nuovi non previsti dallo schema di stampa, è possibile introdurre elementi della proprietà privata. È possibile migliorare o elaborare le informazioni fornite da una proprietà pubblica aggiungendo una o più sottoproprietà private come contenuto dell'elemento della proprietà Public.

Gli elementi della proprietà vengono definiti tramite un tag di elemento XML, <Property> . A ogni proprietà viene assegnato un nome mediante l'attributo Name. Il nome deve essere un QName XML e deve essere conforme alla convenzione dello spazio dei nomi. Per informazioni dettagliate, vedere [attributi XML](xml-attributes.md). L'attributo del nome della proprietà e la relativa posizione all'interno della gerarchia degli elementi della proprietà padre (se si tratta di una sottoproprietà) identificano in modo univoco la proprietà all'interno del documento PrintCapabilities o PrintTicket.

Una proprietà può contenere uno o più elementi value oppure uno o più elementi di proprietà figlio (detti sottoproprietà) o una combinazione di entrambi. Le sottoproprietà sono utili quando la proprietà stessa è costituita da più componenti. Una proprietà "ConsumableColor", ad esempio, può includere i componenti "C", "M" e "Y".

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

 

 




