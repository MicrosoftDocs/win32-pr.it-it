---
description: La tabella ModuleConfiguration identifica gli attributi configurabili del modulo. Questa tabella non è unita nel database.
ms.assetid: 3b77cc23-c104-4adc-868c-3aa2b5794bc7
title: Tabella ModuleConfiguration
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fa187c10b5d3376a9bec78eb897b4982445ff01f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104232070"
---
# <a name="moduleconfiguration-table"></a>Tabella ModuleConfiguration

La tabella ModuleConfiguration identifica gli attributi configurabili del modulo. Questa tabella non è unita nel database.

La tabella ModuleConfiguration include le colonne seguenti.



| Colonna       | Tipo                         | Chiave | Nullable |
|--------------|------------------------------|-----|----------|
| Nome         | [Identificatore](identifier.md) | S   | N        |
| Formato       | [Integer](integer.md)       | N   | N        |
| Tipo         | [Text](text.md)             | N   | S        |
| ContextData  | [Text](text.md)             | N   | S        |
| DefaultValue | [Text](text.md)             | N   | S        |
| Attributi   | [Integer](integer.md)       | N   | S        |
| DisplayName  | [Text](text.md)             | N   | S        |
| Descrizione  | [Text](text.md)             | N   | S        |
| HelpLocation | [Text](text.md)             | N   | S        |
| HelpKeyword  | [Text](text.md)             | N   | S        |



 

## <a name="columns"></a>Colonne

<dl> <dt>

<span id="Name"></span><span id="name"></span><span id="NAME"></span>Nome
</dt> <dd>

Questo campo definisce il nome dell'elemento configurabile. A questo nome viene fatto riferimento nel modello di formattazione della colonna valore della [tabella ModuleSubstitution](modulesubstitution-table.md).

</dd> <dt>

<span id="Format"></span><span id="format"></span><span id="FORMAT"></span>Formato
</dt> <dd>

Questa colonna specifica il formato dei dati da modificare.



| Formato                                       | Valore |
|----------------------------------------------|-------|
| [Text](text-format-types.md)                | 0     |
| [Chiave](key-format-types.md)                  | 1     |
| [Integer](integer-format-types.md)          | 2     |
| [Formato bit](bitfield-format-types.md) | 3     |



 

</dd> <dt>

<span id="Type"></span><span id="type"></span><span id="TYPE"></span>Tipo
</dt> <dd>

In questa colonna viene specificato il tipo per i dati da modificare. Questo tipo viene utilizzato per fornire un contesto per qualsiasi interfaccia utente e non viene utilizzato nel processo di merge. I valori validi per questa colonna dipendono dal valore nella colonna formato.

</dd> <dt>

<span id="ContextData"></span><span id="contextdata"></span><span id="CONTEXTDATA"></span>ContextData
</dt> <dd>

Questa colonna specifica un contesto semantico per i dati richiesti. Il tipo viene utilizzato per fornire un contesto per qualsiasi interfaccia utente e non viene utilizzato nel processo di merge. I valori validi per questa colonna dipendono dai valori nelle colonne format e Type.

</dd> <dt>

<span id="DefaultValue"></span><span id="defaultvalue"></span><span id="DEFAULTVALUE"></span>DefaultValue
</dt> <dd>

In questa colonna viene specificato un valore predefinito per l'elemento in questo record se lo strumento di merge rifiuta di fornire un valore. Questo valore deve avere il formato, il tipo e il contesto dell'elemento. Se si tratta di un elemento di formato "chiave", la chiave esterna deve essere una chiave valida nelle tabelle del modulo. Null può essere un valore valido per questa colonna a seconda dell'elemento. Per gli elementi di formato "Key", questo valore è in [formato speciale CMSM](cmsm-special-format.md). Per tutti gli altri tipi, il valore viene trattato letteralmente.

Gli autori dei moduli devono assicurarsi che il modulo sia valido nello stato predefinito. Ciò garantisce che le versioni di Mergemod.dll precedenti alla versione 2,0 possano ancora usare il modulo nello stato predefinito.

</dd> <dt>

<span id="Attributes"></span><span id="attributes"></span><span id="ATTRIBUTES"></span>Attributi
</dt> <dd>

Questa colonna è un campo di bit contenente gli attributi per questo elemento configurabile. Null equivale a 0. Tutti gli altri bit in questa colonna sono riservati per utilizzi futuri e devono essere pari a 0.



| Nome                             | Decimal | Valore esadecimale | Descrizione                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                         |
|----------------------------------|---------|-------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| msmConfigurableOptionKeyNoOrphan | 1       | 0x00000001  | Questo attributo si applica solo ai record che elencano una chiave esterna di una tabella del modulo nel campo DefaultValue. Lo strumento Merge ignora l'attributo per tutti i formati diversi dai [tipi di formato chiave](key-format-types.md). Gli elementi non elencati nella [tabella ModuleSubstitution](modulesubstitution-table.md) sono esclusi dal controllo seguente. Lo strumento merge non unisce la riga a cui fa riferimento la colonna DefaultValue nel database di destinazione se vengono soddisfatte le condizioni seguenti dopo aver completato tutte le opzioni di configurazione.<br/> Ogni riga della tabella ModuleConfiguration con lo stesso DefaultValue dispone del set di msmConfigurationItemsKeyNoOrphan.<br/> Nessuna riga USA DefaultValue perché lo strumento di creazione ha rifiutato di fornire un valore.<br/> Lo strumento di merge unisce la riga se viene soddisfatta una delle condizioni seguenti.<br/> Lo strumento Merge trova una riga in cui non è impostato msmConfigItemsKeyNoOrphan.<br/> Se lo strumento di merge trova una riga utilizzando DefaultValue perché lo strumento di creazione è stato rifiutato per fornire un valore.<br/> |
| msmConfigurableOptionNonNullable | 2       | 0x00000002  | Quando si imposta questo attributo, null non è una risposta valida per questo elemento. Questo attributo non ha effetto per i tipi di [formato integer](integer-format-types.md) o i [tipi di formato bit](bitfield-format-types.md).                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                    |



 

</dd> <dt>

<span id="DisplayName"></span><span id="displayname"></span><span id="DISPLAYNAME"></span>DisplayName
</dt> <dd>

In questa colonna viene fornita una breve descrizione di questo elemento che può essere utilizzato dallo strumento di creazione nell'interfaccia utente. Questa colonna potrebbe non essere localizzata. Impostare questa colonna su null affinché il modulo richieda che lo strumento di creazione non esponga questa proprietà nell'interfaccia utente. Lo strumento può ignorare il valore in questo campo.

</dd> <dt>

<span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>Descrizione
</dt> <dd>

In questa colonna viene fornita una descrizione di questo elemento che può essere utilizzato da Authoring Tool negli elementi dell'interfaccia utente. Questa stringa può essere localizzata dalla trasformazione della lingua del modulo. Questa colonna può essere null.

</dd> <dt>

<span id="HelpLocation"></span><span id="helplocation"></span><span id="HELPLOCATION"></span>HelpLocation
</dt> <dd>

In questa colonna viene fornito il nome di un file della guida (senza l'estensione chm) o un elenco delimitato da punti e virgola di spazi dei nomi della guida. Questa colonna può essere null se non è disponibile alcuna guida. Questa colonna può essere null solo se la colonna HelpKeyword è null.

</dd> <dt>

<span id="HelpKeyword"></span><span id="helpkeyword"></span><span id="HELPKEYWORD"></span>HelpKeyword
</dt> <dd>

Questa colonna fornisce una parola chiave nel file della guida o nello spazio dei nomi dalla colonna HelpLocation. L'interpretazione di questa parola chiave dipende dalla colonna HelpLocation. Questa colonna può essere null.

</dd> </dl>

## <a name="remarks"></a>Commenti

La tabella ModuleConfiguration viene utilizzata dai [moduli merge configurabili](configurable-merge-modules.md). Per creare un modulo merge configurabile è necessario Mergemod.dll 2,0 o versione successiva.

Per garantire la compatibilità con le versioni precedenti di Mergemod.dll, è necessario aggiungere la tabella ModuleConfiguration e la [tabella ModuleSubstitution](modulesubstitution-table.md) alla [tabella ModuleIgnoreTable](moduleignoretable-table.md) di ogni modulo.

## <a name="validation"></a>Convalida

<dl>

[ICE03](ice03.md)  
[ICE06](ice06.md)  
[ICE25](ice25.md)  
[ICE45](ice45.md)  
</dl>

 

 




