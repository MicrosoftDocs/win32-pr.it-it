---
description: La tabella MsiShortcutProperty consente al programma di installazione di Window di impostare le proprietà per i collegamenti che sono anche oggetti della shell di Windows.
ms.assetid: d959769d-113f-4af2-89d4-ad3f5322de33
title: Tabella MsiShortcutProperty
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f295feabd6ff9b1677fdcf47791959b0fbb8a920
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104529797"
---
# <a name="msishortcutproperty-table"></a>Tabella MsiShortcutProperty

La tabella MsiShortcutProperty consente al programma di installazione di Window di impostare le proprietà per i collegamenti che sono anche oggetti della [Shell di Windows](/previous-versions/windows/desktop/legacy/bb773177(v=vs.85)) . A partire da Windows Vista e Windows Server 2008, la shell di Windows fornisce un'interfaccia IPropertyStore per gli oggetti della shell, ad esempio i collegamenti. Un pacchetto Windows Installer 5,0 in esecuzione in Windows Server 2008 R2 o Windows 7 può impostare queste proprietà quando viene installato il collegamento.

**[Windows Installer 4,5 o versioni precedenti](not-supported-in-windows-installer-4-5.md):** Non supportato. Questa tabella è disponibile a partire da Windows Installer 5,0.

La tabella MsiShortcutProperty include le colonne seguenti.



| Colonna              | Tipo                         | Chiave | Nullable |
|---------------------|------------------------------|-----|----------|
| MsiShortcutProperty | [Identificatore](identifier.md) | S   | N        |
| Tasto di scelta rapida\_          | [Identificatore](identifier.md) | N   | N        |
| PropertyKey         | [Formattato](formatted.md)   | N   | N        |
| PropVariantValue    | [Formattato](formatted.md)   | N   | N        |



 

## <a name="columns"></a>Colonne

<dl> <dt>

<span id="MsiShortcutProperty"></span><span id="msishortcutproperty"></span><span id="MSISHORTCUTPROPERTY"></span>MsiShortcutProperty
</dt> <dd>

Identificatore univoco per questa riga della tabella MsiShortcutProperty.

</dd> <dt>

<span id="Shortcut_"></span><span id="shortcut_"></span><span id="SHORTCUT_"></span>Collegamento\_
</dt> <dd>

Chiave nella tabella dei [collegamenti](shortcut-table.md) che identifica il collegamento con una proprietà impostata.

</dd> <dt>

<span id="PropertyKey"></span><span id="propertykey"></span><span id="PROPERTYKEY"></span>PropertyKey
</dt> <dd>

Valore stringa che fornisce informazioni per la struttura [**PropertyKey**](/windows/win32/api/wtypes/ns-wtypes-propertykey) . Le informazioni contenute in questo campo devono fare riferimento al nome canonico di una proprietà registrata con il sistema di proprietà di Windows. Per ulteriori informazioni sul sistema di proprietà di Windows, vedere [Cenni preliminari sul sistema di proprietà](/previous-versions//bb776909(v=vs.85)).

</dd> <dt>

<span id="PropVariantValue"></span><span id="propvariantvalue"></span><span id="PROPVARIANTVALUE"></span>PropVariantValue
</dt> <dd>

Valore stringa che fornisce informazioni per la struttura [**PROPVARIANT**](/windows/win32/api/propidlbase/ns-propidlbase-propvariant) .

</dd> </dl>

È possibile impostare più proprietà in un collegamento. Se la stessa proprietà viene impostata più volte nello stesso collegamento, il valore viene impostato in un ordine non specificato.

Windows Installer possibile impostare le proprietà dei tasti di scelta rapida solo quando si installa o si reinstalla il collegamento. Una patch che non reinstalla un collegamento che è già stato installato non aggiorna le proprietà del collegamento. Una patch può aggiornare le proprietà includendo una tabella dei [collegamenti](shortcut-table.md) nel pacchetto di patch e reinstallando il collegamento.

## <a name="remarks"></a>Commenti

[Windows Installer messaggio di errore](windows-installer-error-messages.md) 1946 viene restituito come avviso e l'installazione continua, se Windows Installer non è in grado di impostare una proprietà di collegamento specificata nella tabella MsiShortcutProperty.

## <a name="validation"></a>Convalida

<dl>

[ICE03](ice03.md)  
</dl>

 

 
