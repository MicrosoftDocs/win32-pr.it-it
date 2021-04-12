---
description: Per informazioni sugli attributi del controllo, vedere il collegamento al particolare controllo che è necessario creare nei controlli e i collegamenti a specifici attributi di controllo negli elenchi seguenti.
ms.assetid: 948ce3d3-e463-40de-8b5f-21ef18b1a0ce
title: Attributi del controllo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 61d026e84dadefa67ce9d6e00146c6e1c2017cb9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104347791"
---
# <a name="control-attributes"></a>Attributi del controllo

Per informazioni sugli attributi del controllo, vedere il collegamento al particolare controllo che è necessario creare nei [controlli](controls.md) e i collegamenti a specifici attributi di controllo negli elenchi seguenti.

Per specificare gli attributi di un controllo, vengono usati i metodi seguenti:

-   Usare la [tabella ControlCondition](controlcondition-table.md) per disabilitare, abilitare, nascondere o mostrare un controllo in base al valore di una proprietà o di un'istruzione condizionale. È inoltre possibile utilizzare questa tabella per eseguire l'override del controllo predefinito specificato nella [tabella della finestra di dialogo](dialog-table.md).
-   Sottoscrivere il controllo in un ControlEvent nella [tabella EventMapping](eventmapping-table.md). Immettere l'identificatore dell'attributo nella colonna Attribute e l'identificatore di ControlEvent nella colonna Event della tabella.
-   Impostare i flag di bit dell'attributo di controllo per il controllo nella colonna attributo della [tabella dei controlli](control-table.md). Consente di impostare gli attributi durante la creazione del controllo.

Alcuni attributi non possono essere impostati per ogni controllo o essere specificati da tutti i metodi descritti in precedenza. Per informazioni dettagliate, vedere gli argomenti relativi a controlli e attributi specifici.

I valori iniziali di alcuni attributi di controllo possono essere impostati con bit nella [tabella del controllo](control-table.md).



| Attributo                                          | Decimal | Valore esadecimale | Costante                               |
|----------------------------------------------------|---------|-------------|----------------------------------------|
| [BiDi](bidi-control-attribute.md)                 | 224     | 0x000000E0  | **msidbControlAttributesBiDi**         |
| [Enabled](enabled-control-attribute.md)           | 2       | 0x00000002  | **msidbControlAttributesEnabled**      |
| [Indiretto](indirect-control-attribute.md)         | 8       | 0x00000008  | **msidbControlAttributesIndirect**     |
| [Controllo Integer](integer-control-attribute.md)   | 16      | 0x00000010  | **msidbControlAttributesInteger**      |
| [LeftScroll](leftscroll-control-attribute.md)     | 128     | 0x00000080  | **msidbControlAttributesLeftScroll**   |
| [RightAligned](rightaligned-control-attribute.md) | 64      | 0x00000040  | **msidbControlAttributesRightAligned** |
| [RTLRO](rtlro-control-attribute.md)               | 32      | 0x00000020  | **msidbControlAttributesRTLRO**        |
| [Sunken](sunken-control-attribute.md)             | 4       | 0x00000004  | **msidbControlAttributesSunken**       |
| [Visible](visible-control-attribute.md)           | 1       | 0x00000001  | **msidbControlAttributesVisible**      |



 

Questi attributi dei controlli testo sono impostati con BITS.



| Attributo                                            | Decimal | Valore esadecimale | Costante                                |
|------------------------------------------------------|---------|-------------|-----------------------------------------|
| [FormatSize](formatsize-control-attribute.md)       | 524288  | 0x00080000  | **msidbControlAttributesFormatSize**    |
| [NoPrefix](noprefix-control-attribute.md)           | 131072  | 0x00020000  | **msidbControlAttributesNoPrefix**      |
| [NoWrap](nowrap-control-attribute.md)               | 262144  | 0x00040000  | **msidbControlAttributesNoWrap**        |
| [Password](password-control-attribute.md)           | 2097152 | 0x00200000  | **msidbControlAttributesPasswordInput** |
| [Modalità trasparente](transparent-control-attribute.md)     | 65536   | 0x00010000  | **msidbControlAttributesTransparent**   |
| [UsersLanguage](userslanguage-control-attribute.md) | 1048576 | 0x00100000  | **msidbControlAttributesUsersLanguage** |



 

Questo attributo del controllo ProgressBar è impostato su un bit.



| Attributo                                      | Decimal | Valore esadecimale | Costante                             |
|------------------------------------------------|---------|-------------|--------------------------------------|
| [Progress95](progress95-control-attribute.md) | 65536   | 0x00010000  | **msidbControlAttributesProgress95** |



 

Questi attributi dei controlli SelectCombo del volume e della directory sono impostati con BITS.



| Attributo                                                | Decimal | Valore esadecimale | Costante                                  |
|----------------------------------------------------------|---------|-------------|-------------------------------------------|
| [CDROMVolume](cdromvolume-control-attribute.md)         | 524288  | 0x00080000  | **msidbControlAttributesCDROMVolume**     |
| [FixedVolume](fixedvolume-control-attribute.md)         | 131072  | 0x00020000  | **msidbControlAttributesFixedVolume**     |
| [FloppyVolume](floppyvolume-control-attribute.md)       | 2097152 | 0x00200000  | **msidbControlAttributesFloppyVolume**    |
| [RAMDiskVolume](ramdiskvolume-control-attribute.md)     | 1048576 | 0x00100000  | **msidbControlAttributesRAMDiskVolume**   |
| [RemoteVolume](remotevolume-control-attribute.md)       | 262144  | 0x00040000  | **msidbControlAttributesRemoteVolume**    |
| [RemovableVolume](removablevolume-control-attribute.md) | 65536   | 0x00010000  | **msidbControlAttributesRemovableVolume** |



 

Questi attributi dei controlli ListBox e ComboBox sono impostati con BITS.



| Attributo                                            | Decimal | Valore esadecimale | Costante                            |
|------------------------------------------------------|---------|-------------|-------------------------------------|
| [Controllo ComboBox](combolist-control-attribute.md) | 131072  | 0x00020000  | **msidbControlAttributesComboList** |
| [Controllo ordinato](sorted-control-attribute.md)       | 65536   | 0x00010000  | **msidbControlAttributesSorted**    |



 

Questo attributo del controllo di modifica è impostato su un bit.



| Attributo                                    | Decimal | Valore esadecimale | Costante                            |
|----------------------------------------------|---------|-------------|-------------------------------------|
| [MultiLine](multiline-control-attribute.md) | 65536   | 0x00010000  | **msidbControlAttributesMultiline** |



 

Questi attributi dei controlli PictureButton sono impostati con BITS.



| Attributo                                          | Decimal | Valore esadecimale | Costante                             |
|----------------------------------------------------|---------|-------------|--------------------------------------|
| [Bitmap](bitmap-control-attribute.md)             | 262144  | 0x00040000  | **msidbControlAttributesBitmap**     |
| [FixedSize](fixedsize-control-attribute.md)       | 1048576 | 0x00100000  | **msidbControlAttributesFixedSize**  |
| [Icona](icon-control-attribute.md)                 | 524288  | 0x00080000  | **msidbControlAttributesIcon**       |
| [IconSize16](iconsize-control-attribute.md)       | 2097152 | 0x00200000  | **msidbControlAttributesIconSize16** |
| [IconSize32](iconsize-control-attribute.md)       | 4194304 | 0x00400000  | **msidbControlAttributesIconSize32** |
| [IconSize48](iconsize-control-attribute.md)       | 6291456 | 0x00600000  | **msidbControlAttributesIconSize48** |
| [Controllo PushLike](pushlike-control-attribute.md) | 131072  | 0x00020000  | **msidbControlAttributesPushLike**   |



 

Questo attributo del controllo RadioButton è impostato su un bit.



| Attributo                                    | Decimal  | Valore esadecimale | Costante                            |
|----------------------------------------------|----------|-------------|-------------------------------------|
| [HasBorder](hasborder-control-attribute.md) | 16777216 | 0x01000000  | **msidbControlAttributesHasBorder** |



 

Questo attributo del controllo pulsante è impostato su un bit.



| Attributo                                        | Decimal | Valore esadecimale | Costante                                  |
|--------------------------------------------------|---------|-------------|-------------------------------------------|
| [ElevationShield](elevationshield-attribute.md) | 8388608 | 0x00800000  | **msidbControlAttributesElevationShield** |



 

Questo attributo del controllo VolumeCostList è impostato su un bit.



| Attributo                                                                | Decimal | Valore esadecimale | Costante                         |
|--------------------------------------------------------------------------|---------|-------------|----------------------------------|
| [ControlShowRollbackCost](controlshowrollbackcost-control-attribute.md) | 4194304 | 0x00400000  | **msidbControlShowRollbackCost** |



 

Gli attributi di controllo seguenti non sono impostati con BITS. Questi attributi vengono creati nelle tabelle dell'interfaccia utente o vengono impostati utilizzando [gli eventi di controllo](control-events.md).

[Billboardname](billboardname-control-attribute.md)

 

[IndirectPropertyName](indirectpropertyname-control-attribute.md)

 

[Position](position-control-attribute.md)

 

[Controllo dello stato di avanzamento](progress-control-attribute.md)

 

[PropertyName](propertyname-control-attribute.md)

 

[PropertyValue](propertyvalue-control-attribute.md)

 

[Text Control](text-control-attribute.md)

 

[TimeRemaining](timeremaining-control-attribute.md)

Vedere [aggiunta di controlli e testo](adding-controls-and-text.md).

 

 



