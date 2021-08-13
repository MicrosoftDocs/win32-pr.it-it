---
description: I componenti qualificati sono un metodo di riferimento indiretto e possono essere usati per raggruppare i componenti con funzionalità parallele in categorie.
ms.assetid: 45a05ab2-d951-415d-bdb8-cb0a73eb9967
title: Uso di componenti qualificati
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 46c92d165bc06640efea4b8678eeaefa5eb04c36f1b47b6c965faeea00c66adb
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118622947"
---
# <a name="using-qualified-components"></a>Uso di componenti qualificati

I componenti qualificati sono un metodo di riferimento indiretto e possono essere usati per raggruppare i componenti con funzionalità parallele in categorie.

Per restituire il percorso completo e installare un [componente completo,](qualified-components.md)chiamare [**MsiProvideQualifiedComponent**](/windows/desktop/api/Msi/nf-msi-msiprovidequalifiedcomponenta) o [**MsiProvideQualifiedComponentEx**](/windows/desktop/api/Msi/nf-msi-msiprovidequalifiedcomponentexa).

Per enumerare tutti i qualificatori di componenti qualificati e le stringhe descrittive, chiamare [**MsiEnumComponentQualifiers**](/windows/desktop/api/Msi/nf-msi-msienumcomponentqualifiersa).

**Per raggruppare i componenti in una categoria di componenti qualificati**

1.  Nella tabella Componente deve essere presente un record [per](component-table.md) ogni componente incluso nella nuova categoria di componenti qualificati. Creare i campi nella tabella Componente come per i componenti ordinari. Si noti che ogni componente qualificato deve avere un GUID ID componente univoco immesso nella colonna ComponentId della tabella Component.
2.  Generare una stringa di testo del qualificatore per ogni componente qualificato. Il qualificatore deve essere una stringa di testo univoca che può essere generata facilmente durante la ricerca di un componente completo. Ad esempio, se i componenti della categoria vengono qualificati in base alla lingua, l'identificatore delle impostazioni locali numerico (LCID) è una stringa di qualificatore ragionevole.
3.  Aggiungere un record nella [tabella PublishComponent per](publishcomponent-table.md) ogni componente completo. Immettere gli identificatori dei componenti qualificati dalla colonna Componente della tabella Componente nella colonna Componente \_ della tabella PublishComponent. Immettere le stringhe di qualificatore per ogni componente qualificato nella colonna Qualificatore. Immettere una stringa localizzata da visualizzare all'utente e descrivere il componente completo nella colonna AppData facoltativa. Nel campo AppData deve essere inserita una stringa esplicativa, ad esempio "Dizionario francese", anziché solo l'LCID numerico. Immettere il nome della funzionalità che usa questo componente nella colonna \_ Funzionalità. L'identificatore di funzionalità in questo campo deve essere elencato anche nella colonna Funzionalità della [tabella Funzionalità](feature-table.md).
4.  Generare un GUID di categoria per questa categoria di componenti qualificati. Deve essere un [GUID valido.](guid.md) Se si usa un'utilità come GUIDGEN per generare il GUID, assicurarsi che contenga solo lettere maiuscole. Per ogni componente qualificato in questa categoria, immettere il GUID della categoria nel campo ComponentId della [tabella PublishComponent](publishcomponent-table.md).

Nell'esempio seguente viene illustrata la creazione della categoria "Modelli FAX" di componenti qualificati nelle tabelle Component, Feature e PublishComponent.

[Tabella PublishComponent](publishcomponent-table.md)



| Componentid                  | Qualifier | AppData             | Funzionalità\_   | Componente\_    |
|------------------------------|-----------|---------------------|-------------|----------------|
| {GUID categoria modello FAX} | 1033      | Modello inglese degli Stati Uniti | FAXTemplate | FAXTemplateENU |
|                              | 1041      | Modello giapponese   | FAXTemplate | FAXTemplateJPN |
|                              | 1054      | Modello tailandese       | FAXTemplate | FAXTemplateTHA |
|                              | 1031      | Modello tedesco     | FAXTemplate | FAXTemplateDEU |



 

[Tabella dei componenti](component-table.md) (tabella parziale)



| Componente      | Componentid                                  |
|----------------|----------------------------------------------|
| FAXTemplateENU | {*FAX Template (US English) component GUID*} |
| FAXTemplateJPN | {*FAX Template (Japanese) component GUID*}   |
| FAXTemplateTHA | {*FAX Template (Thai) component GUID*}       |
| FAXTemplateDEU | {*FAX Template (German) component GUID*}     |



 

[Tabella delle funzionalità](feature-table.md) (tabella parziale)



| Funzionalità     |
|-------------|
| FAXTemplate |
| FAXTemplate |
| FAXTemplate |
| FAXTemplate |



 

 

 



