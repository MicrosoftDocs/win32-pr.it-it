---
description: La tabella MsiShortcutProperty consente a Windows Installer di impostare le proprietà per i collegamenti Windows shell.
ms.assetid: d959769d-113f-4af2-89d4-ad3f5322de33
title: Tabella MsiShortcutProperty
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4d7cf51d8016cdc87008a6cc9a20daee1f35131af7ea0f5827c67da7f45a6e46
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118944428"
---
# <a name="msishortcutproperty-table"></a>Tabella MsiShortcutProperty

La tabella MsiShortcutProperty consente a Windows Installer di impostare le proprietà per i collegamenti Windows [oggetti shell.](/previous-versions/windows/desktop/legacy/bb773177(v=vs.85)) A partire da Windows Vista e Windows Server 2008, Windows Shell fornisce un'interfaccia IPropertyStore per gli oggetti della shell, ad esempio i collegamenti. Un pacchetto Windows Installer 5.0 in esecuzione in Windows Server 2008 R2 o Windows 7 può impostare queste proprietà quando viene installato il collegamento.

**[Windows Installer 4.5 o versioni precedenti:](not-supported-in-windows-installer-4-5.md)** Non supportato. Questa tabella è disponibile a partire da Windows Installer 5.0.

La tabella MsiShortcutProperty contiene le colonne seguenti.



| Colonna              | Tipo                         | Chiave | Nullable |
|---------------------|------------------------------|-----|----------|
| Proprietà MsiShortcutProperty | [Identificatore](identifier.md) | S   | N        |
| Tasto di scelta rapida\_          | [Identificatore](identifier.md) | N   | N        |
| PropertyKey         | [Formattato](formatted.md)   | N   | N        |
| PropVariantValue    | [Formattato](formatted.md)   | N   | N        |



 

## <a name="columns"></a>Colonne

<dl> <dt>

<span id="MsiShortcutProperty"></span><span id="msishortcutproperty"></span><span id="MSISHORTCUTPROPERTY"></span>Proprietà MsiShortcutProperty
</dt> <dd>

Identificatore univoco per questa riga della tabella MsiShortcutProperty.

</dd> <dt>

<span id="Shortcut_"></span><span id="shortcut_"></span><span id="SHORTCUT_"></span>Scelta rapida\_
</dt> <dd>

Tasto nella tabella [Collegamento](shortcut-table.md) che identifica il collegamento con una proprietà impostata.

</dd> <dt>

<span id="PropertyKey"></span><span id="propertykey"></span><span id="PROPERTYKEY"></span>PropertyKey
</dt> <dd>

Valore stringa che fornisce informazioni per la [**struttura PROPERTYKEY.**](/windows/win32/api/wtypes/ns-wtypes-propertykey) Le informazioni contenute in questo campo devono fare riferimento al nome canonico di una proprietà registrata con il Windows proprietà. Per altre informazioni sul sistema Windows proprietà, vedere [Cenni preliminari sul sistema di proprietà](/previous-versions//bb776909(v=vs.85)).

</dd> <dt>

<span id="PropVariantValue"></span><span id="propvariantvalue"></span><span id="PROPVARIANTVALUE"></span>PropVariantValue
</dt> <dd>

Valore stringa che fornisce informazioni per la [**struttura PROPVARIANT.**](/windows/win32/api/propidlbase/ns-propidlbase-propvariant)

</dd> </dl>

È possibile impostare più proprietà in un collegamento. Se la stessa proprietà viene impostata più volte sullo stesso collegamento, il valore viene impostato in un ordine non specificato.

Windows Il programma di installazione può impostare le proprietà dei collegamenti solo quando il collegamento viene installato o reinstallato. Una patch che non reinstalla un collegamento già installato non aggiorna le proprietà del collegamento. Una patch può aggiornare le proprietà includendo una [tabella Collegamento](shortcut-table.md) nel pacchetto di patch e reinstallando il collegamento.

## <a name="remarks"></a>Commenti

[Windows messaggio](windows-installer-error-messages.md) di errore del programma di installazione 1946 viene restituito come avviso e l'installazione continua se Windows Installer non è in grado di impostare una proprietà di collegamento specificata nella tabella MsiShortcutProperty.

## <a name="validation"></a>Convalida

<dl>

[ICE03](ice03.md)  
</dl>

 

 
