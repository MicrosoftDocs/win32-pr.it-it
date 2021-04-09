---
description: I componenti qualificati sono un metodo di riferimento indiretto e possono essere usati per raggruppare componenti con funzionalità parallele in categorie.
ms.assetid: 45a05ab2-d951-415d-bdb8-cb0a73eb9967
title: Utilizzo di componenti qualificati
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d11233a91e8883d1a4151957d3e73d18ebdcff25
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104129358"
---
# <a name="using-qualified-components"></a>Utilizzo di componenti qualificati

I componenti qualificati sono un metodo di riferimento indiretto e possono essere usati per raggruppare componenti con funzionalità parallele in categorie.

Per restituire il percorso completo e installare un [componente completo](qualified-components.md), chiamare [**MsiProvideQualifiedComponent**](/windows/desktop/api/Msi/nf-msi-msiprovidequalifiedcomponenta) o [**MsiProvideQualifiedComponentEx**](/windows/desktop/api/Msi/nf-msi-msiprovidequalifiedcomponentexa).

Per enumerare tutti i qualificatori del componente completo e le stringhe descrittive, chiamare [**MsiEnumComponentQualifiers**](/windows/desktop/api/Msi/nf-msi-msienumcomponentqualifiersa).

**Per raggruppare i componenti in una categoria di componenti qualificati**

1.  È necessario che nella [tabella](component-table.md) dei componenti sia presente un record per ogni componente incluso nella nuova categoria di componenti qualificati. Modificare i campi nella tabella dei componenti come per i componenti ordinari. Si noti che ogni componente qualificato deve avere un GUID ID componente univoco immesso nella colonna ComponentId della tabella Component.
2.  Genera una stringa di testo qualificatore per ogni componente completo. Il qualificatore deve essere una stringa di testo univoca che può essere generata facilmente durante la ricerca di un componente completo. Se, ad esempio, i componenti della categoria vengono qualificati in base alla lingua, l'identificatore delle impostazioni locali (LCID) numerico è una stringa di qualificatore ragionevole.
3.  Aggiungere un record nella [tabella PublishComponent](publishcomponent-table.md) per ogni componente completo. Immettere gli identificatori dei componenti completi dalla colonna componente della tabella Component nella \_ colonna Component della tabella PublishComponent. Immettere le stringhe di qualificatore per ogni componente qualificato nella colonna qualificatore. Immettere una stringa localizzata da visualizzare all'utente e descrivere il componente qualificato nella colonna AppData facoltativa. È necessario inserire nel campo AppData una stringa esplicativa, ad esempio "dizionario francese", anziché solo l'identificatore LCID numerico. Immettere il nome della funzionalità che utilizza questo componente nella \_ colonna feature. L'identificatore di funzionalità in questo campo deve essere elencato anche nella colonna feature della [tabella Feature](feature-table.md).
4.  Genera un GUID di categoria per questa categoria di componenti qualificati. Deve essere un [GUID](guid.md)valido. Se si usa un'utilità come GUIDGEN per generare il GUID, assicurarsi che contenga solo lettere maiuscole. Per ogni componente qualificato in questa categoria, immettere il GUID della categoria nel campo ComponentId della [tabella PublishComponent](publishcomponent-table.md).

Nell'esempio seguente viene illustrato il modo in cui viene creata la categoria "modelli FAX" di componenti qualificati nelle tabelle componente, funzionalità e PublishComponent.

[Tabella PublishComponent](publishcomponent-table.md)



| ComponentId                  | Qualifier | AppData             | Funzionalità\_   | Componente\_    |
|------------------------------|-----------|---------------------|-------------|----------------|
| {GUID categoria modello FAX} | 1033      | Modello di inglese (Stati Uniti) | FAXTemplate | FAXTemplateENU |
|                              | 1041      | Modello giapponese   | FAXTemplate | FAXTemplateJPN |
|                              | 1054      | Modello tailandese       | FAXTemplate | FAXTemplateTHA |
|                              | 1031      | Modello tedesco     | FAXTemplate | FAXTemplateDEU |



 

[Tabella componenti](component-table.md) (tabella parziale)



| Componente      | ComponentId                                  |
|----------------|----------------------------------------------|
| FAXTemplateENU | {*Modello Fax (Inglese Stati Uniti) GUID componente*} |
| FAXTemplateJPN | {*GUID componente (giapponese) del modello Fax*}   |
| FAXTemplateTHA | {*GUID del componente del modello Fax (Thai)*}       |
| FAXTemplateDEU | {*Modello Fax (tedesco) GUID componente*}     |



 

[Tabella Feature](feature-table.md) (tabella parziale)



| Funzionalità     |
|-------------|
| FAXTemplate |
| FAXTemplate |
| FAXTemplate |
| FAXTemplate |



 

 

 



