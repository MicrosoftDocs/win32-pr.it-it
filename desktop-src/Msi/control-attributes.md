---
description: Per informazioni sugli attributi del controllo, vedere il collegamento al controllo specifico che è necessario creare in Controls, nonché i collegamenti a particolari attributi del controllo negli elenchi seguenti.
ms.assetid: 948ce3d3-e463-40de-8b5f-21ef18b1a0ce
title: Attributi del controllo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: eb9d7412ce3893b785dccf067287c191f033bdf5a100628577260ff10f74ce1e
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119500721"
---
# <a name="control-attributes"></a>Attributi del controllo

Per informazioni sugli attributi del controllo, vedere il collegamento al controllo specifico che è necessario creare in [Controls,](controls.md) nonché i collegamenti a particolari attributi del controllo negli elenchi seguenti.

Per specificare gli attributi di un controllo vengono usati i metodi seguenti:

-   Usare la [tabella ControlCondition per](controlcondition-table.md) disabilitare, abilitare, nascondere o visualizzare un controllo in base al valore di una proprietà o di un'istruzione condizionale. È anche possibile usare questa tabella per eseguire l'override del controllo predefinito specificato nella [tabella Dialog](dialog-table.md).
-   Sottoscrivere il controllo a un ControlEvent nella [tabella EventMapping](eventmapping-table.md). Immettere l'identificatore dell'attributo nella colonna Attributo e l'identificatore di ControlEvent nella colonna Event di questa tabella.
-   Impostare i flag di bit dell'attributo del controllo per il controllo nella colonna Attribute della [tabella Control](control-table.md). In questo modo gli attributi vengono impostate al momento della creazione del controllo.

Alcuni attributi non possono essere impostati per ogni controllo o essere specificati da tutti i metodi precedenti. Per informazioni dettagliate, vedere gli argomenti relativi a controlli e attributi specifici.

I valori iniziali di alcuni attributi di controllo possono essere impostati con bit nella [tabella Control](control-table.md).



| Attributo                                          | Decimal | Valore esadecimale | Costante                               |
|----------------------------------------------------|---------|-------------|----------------------------------------|
| [Bidi](bidi-control-attribute.md)                 | 224     | 0x000000E0  | **msidbControlAttributesBiDi**         |
| [Enabled](enabled-control-attribute.md)           | 2       | 0x00000002  | **msidbControlAttributesEnabled**      |
| [Indiretto](indirect-control-attribute.md)         | 8       | 0x00000008  | **msidbControlAttributesIndirect**     |
| [Controllo Integer](integer-control-attribute.md)   | 16      | 0x00000010  | **msidbControlAttributesInteger**      |
| [LeftScroll](leftscroll-control-attribute.md)     | 128     | 0x00000080  | **msidbControlAttributesLeftScroll**   |
| [RightAligned](rightaligned-control-attribute.md) | 64      | 0x00000040  | **msidbControlAttributesRightAligned** |
| [RTLRO](rtlro-control-attribute.md)               | 32      | 0x00000020  | **msidbControlAttributesRTLRO**        |
| [Sunken](sunken-control-attribute.md)             | 4       | 0x00000004  | **msidbControlAttributesSunken**       |
| [Visible](visible-control-attribute.md)           | 1       | 0x00000001  | **msidbControlAttributesVisible**      |



 

Questi attributi dei controlli Text sono impostati con bit.



| Attributo                                            | Decimal | Valore esadecimale | Costante                                |
|------------------------------------------------------|---------|-------------|-----------------------------------------|
| [FormatSize](formatsize-control-attribute.md)       | 524288  | 0x00080000  | **msidbControlAttributesFormatSize**    |
| [NoPrefix](noprefix-control-attribute.md)           | 131072  | 0x00020000  | **msidbControlAttributesNoPrefix**      |
| [Nowrap](nowrap-control-attribute.md)               | 262144  | 0x00040000  | **msidbControlAttributesNoWrap**        |
| [Password](password-control-attribute.md)           | 2097152 | 0x00200000  | **msidbControlAttributesPasswordInput** |
| [Modalità trasparente](transparent-control-attribute.md)     | 65536   | 0x00010000  | **msidbControlAttributesTransparent**   |
| [UtentiLingua](userslanguage-control-attribute.md) | 1048576 | 0x00100000  | **msidbControlAttributesUsersLanguage** |



 

Questo attributo del controllo ProgressBar è impostato con un bit.



| Attributo                                      | Decimal | Valore esadecimale | Costante                             |
|------------------------------------------------|---------|-------------|--------------------------------------|
| [Stato di avanzamento95](progress95-control-attribute.md) | 65536   | 0x00010000  | **msidbControlAttributesProgress95** |



 

Questi attributi dei controlli Volume e Directory SelectCombo sono impostati con bit.



| Attributo                                                | Decimal | Valore esadecimale | Costante                                  |
|----------------------------------------------------------|---------|-------------|-------------------------------------------|
| [CDROMVolume](cdromvolume-control-attribute.md)         | 524288  | 0x00080000  | **msidbControlAttributesCDROMVolume**     |
| [FixedVolume](fixedvolume-control-attribute.md)         | 131072  | 0x00020000  | **msidbControlAttributesFixedVolume**     |
| [FloppyVolume](floppyvolume-control-attribute.md)       | 2097152 | 0x00200000  | **msidbControlAttributesFloppyVolume**    |
| [RAMDiskVolume](ramdiskvolume-control-attribute.md)     | 1048576 | 0x00100000  | **msidbControlAttributesRAMDiskVolume**   |
| [RemoteVolume](remotevolume-control-attribute.md)       | 262144  | 0x00040000  | **msidbControlAttributesRemoteVolume**    |
| [RemovableVolume](removablevolume-control-attribute.md) | 65536   | 0x00010000  | **msidbControlAttributesRemovableVolume** |



 

Questi attributi dei controlli ListBox e ComboBox sono impostati con bit.



| Attributo                                            | Decimal | Valore esadecimale | Costante                            |
|------------------------------------------------------|---------|-------------|-------------------------------------|
| [Controllo ComboList](combolist-control-attribute.md) | 131072  | 0x00020000  | **msidbControlAttributesComboList** |
| [Controllo ordinato](sorted-control-attribute.md)       | 65536   | 0x00010000  | **msidbControlAttributesSorted**    |



 

Questo attributo del controllo Edit è impostato con un bit.



| Attributo                                    | Decimal | Valore esadecimale | Costante                            |
|----------------------------------------------|---------|-------------|-------------------------------------|
| [Multilinea](multiline-control-attribute.md) | 65536   | 0x00010000  | **msidbControlAttributesMultiline** |



 

Questi attributi dei controlli PictureButton sono impostati con bit.



| Attributo                                          | Decimal | Valore esadecimale | Costante                             |
|----------------------------------------------------|---------|-------------|--------------------------------------|
| [Bitmap](bitmap-control-attribute.md)             | 262144  | 0x00040000  | **msidbControlAttributesBitmap**     |
| [FixedSize](fixedsize-control-attribute.md)       | 1048576 | 0x00100000  | **msidbControlAttributesFixedSize**  |
| [Icona](icon-control-attribute.md)                 | 524288  | 0x00080000  | **msidbControlAttributesIcon**       |
| [IconSize16](iconsize-control-attribute.md)       | 2097152 | 0x00200000  | **msidbControlAttributesIconSize16** |
| [IconSize32](iconsize-control-attribute.md)       | 4194304 | 0x00400000  | **msidbControlAttributesIconSize32** |
| [IconSize48](iconsize-control-attribute.md)       | 6291456 | 0x00600000  | **msidbControlAttributesIconSize48** |
| [Controllo PushLike](pushlike-control-attribute.md) | 131072  | 0x00020000  | **msidbControlAttributesPushLike**   |



 

Questo attributo del controllo RadioButton è impostato con un bit.



| Attributo                                    | Decimal  | Valore esadecimale | Costante                            |
|----------------------------------------------|----------|-------------|-------------------------------------|
| [HasBorder](hasborder-control-attribute.md) | 16777216 | 0x01000000  | **msidbControlAttributesHasBorder** |



 

Questo attributo del controllo PushButton è impostato con un bit.



| Attributo                                        | Decimal | Valore esadecimale | Costante                                  |
|--------------------------------------------------|---------|-------------|-------------------------------------------|
| [ElevationShield](elevationshield-attribute.md) | 8388608 | 0x00800000  | **msidbControlAttributesElevationShield** |



 

Questo attributo del controllo VolumeCostList è impostato con un bit.



| Attributo                                                                | Decimal | Valore esadecimale | Costante                         |
|--------------------------------------------------------------------------|---------|-------------|----------------------------------|
| [ControlShowRollbackCost](controlshowrollbackcost-control-attribute.md) | 4194304 | 0x00400000  | **msidbControlShowRollbackCost** |



 

Gli attributi di controllo seguenti non sono impostati con bit. Questi attributi vengono creati nelle tabelle dell'interfaccia utente o vengono impostati tramite Eventi [di controllo](control-events.md).

[NomeSezione](billboardname-control-attribute.md)

 

[IndirectPropertyName](indirectpropertyname-control-attribute.md)

 

[Position](position-control-attribute.md)

 

[Controllo Progress](progress-control-attribute.md)

 

[PropertyName](propertyname-control-attribute.md)

 

[PropertyValue](propertyvalue-control-attribute.md)

 

[Text Control](text-control-attribute.md)

 

[TimeRemaining](timeremaining-control-attribute.md)

Vedere [Aggiunta di controlli e testo.](adding-controls-and-text.md)

 

 



