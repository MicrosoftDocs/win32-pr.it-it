---
description: La tabella di aggiornamento contiene le informazioni necessarie durante gli aggiornamenti principali.
ms.assetid: f5fda405-8a09-495e-aa8c-b808a2f02b0f
title: Aggiorna tabella
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6b48ce49f0f931209ccf472cd74b352c270353a2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104348961"
---
# <a name="upgrade-table"></a>Aggiorna tabella

La tabella di aggiornamento contiene le informazioni necessarie durante gli [aggiornamenti principali](major-upgrades.md). Per abilitare completamente le funzionalità di aggiornamento del programma di installazione, ogni pacchetto deve disporre di una proprietà [**UpgradeCode**](upgradecode.md) e di una tabella di aggiornamento. Ogni record nella tabella di aggiornamento fornisce una caratteristica combinazione del codice di aggiornamento, della versione del prodotto e delle informazioni sulla lingua utilizzate per identificare un set di prodotti interessati dall'aggiornamento. Quando l'azione [FindRelatedProducts](findrelatedproducts-action.md) rileva un prodotto interessato installato nel sistema, aggiunge il codice prodotto a una proprietà specificata nella colonna ActionProperty. L'azione [RemoveExistingProducts](removeexistingproducts-action.md) e l'azione [MigrateFeatureStates](migratefeaturestates-action.md) rimuovono o migrano solo i prodotti elencati nella colonna ActionProperty.

La tabella di aggiornamento contiene le colonne mostrate nella tabella seguente.



| Colonna         | Tipo                         | Chiave | Nullable |
|----------------|------------------------------|-----|----------|
| UpgradeCode    | [GUID](guid.md)             | S   | N        |
| VersionMin     | [Text](text.md)             | S   | S        |
| VersionMax     | [Text](text.md)             | S   | S        |
| Linguaggio       | [Text](text.md)             | S   | S        |
| Attributi     | [Integer](integer.md)       | S   | N        |
| Rimuovi         | [Formattato](formatted.md)   | N   | S        |
| ActionProperty | [Identificatore](identifier.md) | N   | N        |



 

## <a name="columns"></a>Colonne

<dl> <dt>

<span id="UpgradeCode"></span><span id="upgradecode"></span><span id="UPGRADECODE"></span>UpgradeCode
</dt> <dd>

La proprietà [UpgradeCode](upgradecode.md) in questa colonna specifica il codice di aggiornamento di tutti i prodotti che devono essere rilevati dall'azione [FindRelatedProducts](findrelatedproducts-action.md) .

</dd> <dt>

<span id="VersionMin"></span><span id="versionmin"></span><span id="VERSIONMIN"></span>VersionMin
</dt> <dd>

Limite inferiore dell'intervallo di versioni del prodotto rilevate da [FindRelatedProducts](findrelatedproducts-action.md). Immettere **msidbUpgradeAttributesVersionMinInclusive** negli attributi per includere VersionMin nell'intervallo. Se VersionMin è uguale a una stringa vuota (""), viene valutato come 0. Se VersionMin è null, FindRelatedProducts ignora **msidbUpgradeAttributesVersionMinInclusive** e rileva tutte le versioni precedenti. VersionMin e VersionMax non devono essere entrambi null.

VersionMin deve essere una versione di prodotto valida come descritto per la proprietà [**ProductVersion**](productversion.md) . Si noti che Windows Installer utilizza solo i primi tre campi della versione del prodotto. Se si include un quarto campo nella versione del prodotto, il programma di installazione ignorerà il quarto campo.

</dd> <dt>

<span id="VersionMax"></span><span id="versionmax"></span><span id="VERSIONMAX"></span>VersionMax
</dt> <dd>

Limite superiore dell'intervallo di versioni del prodotto rilevato dall'azione [FindRelatedProducts](findrelatedproducts-action.md) . Immettere **msidbUpgradeAttributesVersionMaxInclusive** negli attributi per includere VersionMax nell'intervallo. Se VersionMax è una stringa vuota (""), viene valutata come uguale a 0. Se VersionMax è null, FindRelatedProducts ignora **msidbUpgradeAttributesVersionMaxInclusive** e rileva tutte le versioni di prodotto maggiori di (o maggiori o uguali a) il limite inferiore specificato da VersionMin e **msidbUpgradeAttributesVersionMinInclusive**. VersionMin e VersionMax non devono essere entrambi null.

VersionMax deve essere una versione di prodotto valida come descritto per la proprietà [**ProductVersion**](productversion.md) . Si noti che Windows Installer utilizza solo i primi tre campi della versione del prodotto. Se si include un quarto campo nella versione del prodotto, il programma di installazione ignorerà il quarto campo.

</dd> <dt>

<span id="Language"></span><span id="language"></span><span id="LANGUAGE"></span>Linguaggio
</dt> <dd>

Set di lingue rilevate da [FindRelatedProducts](findrelatedproducts-action.md). Immettere un elenco di identificatori di lingua numerici (LANGID) separati da virgole. Immettere **msidbUpgradeAttributesLanguagesExclusive** negli attributi per rilevare tutte le lingue esclusive di quelle elencate in lingua. Se Language è null o una stringa vuota (""), FindRelatedProducts ignora **msidbUpgradeAttributesLanguagesExclusive** e rileva tutte le lingue.

</dd> <dt>

<span id="Attributes"></span><span id="attributes"></span><span id="ATTRIBUTES"></span>Attributi
</dt> <dd>

Questa colonna contiene flag di bit che specificano gli attributi della tabella di aggiornamento.



| Nome del flag di bit                                 | Decimal | Valore esadecimale | Attributo                                                                                                            |
|-----------------------------------------------|---------|-------------|----------------------------------------------------------------------------------------------------------------------|
| **msidbUpgradeAttributesMigrateFeatures**     | 1       | 0x001       | Esegue la migrazione degli Stati delle funzionalità abilitando la logica nell'azione [MigrateFeatureStates](migratefeaturestates-action.md) . |
| **msidbUpgradeAttributesOnlyDetect**          | 2       | 0x002       | Rileva i prodotti e le applicazioni, ma non rimuove.                                                               |
| **msidbUpgradeAttributesIgnoreRemoveFailure** | 4       | 0x004       | Continua l'installazione in caso di errore durante la rimozione di un prodotto o di un'applicazione.                                              |
| **msidbUpgradeAttributesVersionMinInclusive** | 256     | 0x100       | Rileva l'intervallo di versioni compreso il valore in VersionMin.                                                     |
| **msidbUpgradeAttributesVersionMaxInclusive** | 512     | 0x200       | Rileva l'intervallo di versioni compreso il valore in VersionMax.                                                     |
| **msidbUpgradeAttributesLanguagesExclusive**  | 1024    | 0x400       | Rileva tutte le lingue, escluse le lingue elencate nella colonna lingua.                                        |



 

</dd> <dt>

<span id="Remove"></span><span id="remove"></span><span id="REMOVE"></span>Rimuovere
</dt> <dd>

Il programma di installazione imposta la proprietà [**Remove**](remove.md) sulle funzionalità specificate in questa colonna. Le funzionalità da rimuovere possono essere determinate in fase di esecuzione. La stringa [formattata](formatted.md) immessa in questo campo deve restituire un elenco delimitato da virgole di nomi di funzionalità. Ad esempio: \[ Feature1 \] , \[ Funzionalità2 \] , \[ feature3 \] . Nessuna funzionalità viene rimossa se il campo contiene testo formattato che restituisce una stringa vuota (""). Il programma di installazione imposta REMOVE = ALL solo se il campo Remove è vuoto. Si noti la differenza tra una stringa vuota e un campo vuoto. Se il campo è vuoto, è null.

</dd> <dt>

<span id="ActionProperty"></span><span id="actionproperty"></span><span id="ACTIONPROPERTY"></span>ActionProperty
</dt> <dd>

Quando l'azione [FindRelatedProducts](findrelatedproducts-action.md) rileva un prodotto correlato installato nel sistema, aggiunge il codice prodotto alla proprietà specificata in questo campo. La proprietà specificata in questa colonna deve essere una proprietà pubblica e l'autore del pacchetto deve aggiungere la proprietà alla proprietà [**SecureCustomProperties**](securecustomproperties.md) . Ogni riga della tabella di aggiornamento deve avere un valore ActionProperty univoco. Dopo FindRelatedProducts, il valore di questa proprietà è un elenco di codici prodotto, separati da punti e virgola (;), rilevato nel sistema.

</dd> </dl>

## <a name="validation"></a>Convalida

<dl>

[ICE03](ice03.md)  
[ICE06](ice06.md)  
[ICE46](ice46.md)  
[ICE61](ice61.md)  
[ICE66](ice66.md)  
</dl>

 

 



