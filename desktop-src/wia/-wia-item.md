---
description: I dispositivi hardware Windows Image Acquisition (WIA) sono rappresentati come alberi gerarchici di oggetti elemento. L'elemento radice di questo albero rappresenta il dispositivo stesso, mentre gli elementi figlio rappresentano immagini, cartelle o letti di analisi.
ms.assetid: 240557d6-665e-4879-8c6e-f564ca61e031
title: Oggetto Item
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Item
api_type:
- COM
api_location:
- Wiascr.dll
ms.openlocfilehash: 6af0642a47db9d3a7a1c30aea76be22ea5ce1d07
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103752847"
---
# <a name="item-object"></a>Oggetto Item

I dispositivi hardware Windows Image Acquisition (WIA) sono rappresentati come alberi gerarchici di oggetti **elemento** . L'elemento radice di questo albero rappresenta il dispositivo stesso, mentre gli elementi figlio rappresentano immagini, cartelle o letti di analisi.

Usare l'oggetto **Item** per trasferire i dati in un file, per spostarsi nell'albero degli elementi per un determinato dispositivo o per recuperare informazioni su un'immagine o un dispositivo.

## <a name="members"></a>Membri

L'oggetto **Item** presenta questi tipi di membri:

-   [Metodi](#methods)
-   [Proprietà](#properties)

### <a name="methods"></a>Metodi

L'oggetto **Item** presenta questi metodi.



| Metodo                                                         | Descrizione                                                                                                                                                                                                                                                                    |
|:---------------------------------------------------------------|:-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**GetItemsFromUI**](-wia-iwiadispatchitem-getitemsfromui.md) | Il metodo [**GetItemsFromUI**](-wia-iwiadispatchitem-getitemsfromui.md) dell'oggetto **Item** Visualizza una finestra di dialogo che consente a un utente di selezionare immagini e audio da trasferire da un dispositivo.<br/>                                                                     |
| [**GetPropById**](-wia-iwiadispatchitem-getpropbyid.md)       | Il metodo [**GetPropById**](-wia-iwiadispatchitem-getpropbyid.md) dell'oggetto **Item** usa l'ID di una proprietà Item per restituirne il valore.<br/>                                                                                                                     |
| [**TakePicture**](-wia-iwiadispatchitem-takepicture.md)       | Il metodo [**TakePicture**](-wia-iwiadispatchitem-takepicture.md) dell'oggetto **Item** fa in modo che un dispositivo della fotocamera digitale prenda un'immagine e restituisce un oggetto **Item** che rappresenta l'immagine risultante. Questo metodo si applica solo ai dispositivi della fotocamera digitale.<br/> |
| [**Trasferimento**](-wia-iwiadispatchitem-transfer.md)             | Il metodo di [**trasferimento**](-wia-iwiadispatchitem-transfer.md) dell'oggetto **Item** trasferisce i dati da un dispositivo a un file. Questo metodo si applica solo agli elementi del tipo di dispositivo.<br/>                                                                                         |



 

### <a name="properties"></a>Proprietà

L'oggetto **Item** dispone di queste proprietà.



| Proprietà                                                                    | Tipo di accesso          | Descrizione                                                                                                                                                                                                                                                 |
|:----------------------------------------------------------------------------|:---------------------|:------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Children**](-wia-iwiadispatchitem-children.md)<br/>               | Sola lettura<br/> | La proprietà [**Children**](-wia-iwiadispatchitem-children.md) dell'oggetto **Item** recupera una raccolta di oggetti **Item** . Gli elementi in questa raccolta rappresentano elementi che sono elementi figlio diretti di questo elemento nell'albero gerarchico. <br/> |
| [**ConnectStatus**](-wia-iwiadispatchitem-connectstatus.md)<br/>     | Sola lettura<br/> | Recupera lo stato della connessione del dispositivo. Questa proprietà si applica solo agli elementi di tipo Device (elementi radice). I valori possibili sono "Connected", "Disconnected" o **null** (se questa proprietà non è applicabile all'elemento). <br/>                     |
| [**FirmwareVersion**](-wia-iwiadispatchitem-firmwareversion.md)<br/> | Sola lettura<br/> | Recupera la versione del firmware del dispositivo. Questa proprietà si applica solo agli elementi di tipo Device (elementi radice). <br/>                                                                                                                                  |
| [**FullName**](-wia-iwiadispatchitem-fullname.md)<br/>               | Sola lettura<br/> | Recupera il nome completo dell'elemento visualizzato nell'interfaccia utente. <br/>                                                                                                                                                                                    |
| [**Altezza**](-wia-iwiadispatchitem-height.md)<br/>                   | Sola lettura<br/> | Altezza, in pixel, dell'elemento. <br/>                                                                                                                                                                                                             |
| [**ItemType**](-wia-iwiadispatchitem-itemtype.md)<br/>               | Sola lettura<br/> | Tipo di questo elemento. <br/>                                                                                                                                                                                                                          |
| [**Nome**](-wia-iwiadispatchitem-name.md)<br/>                       | Sola lettura<br/> | Nome dell'elemento visualizzato nell'interfaccia utente. <br/>                                                                                                                                                                                                   |
| [**PictureHeight**](-wia-iwiadispatchitem-pictureheight.md)<br/>     | Sola lettura<br/> | Altezza, in pixel, delle immagini prodotte da questa fotocamera digitale. Si applica solo alle fotocamere digitali. <br/>                                                                                                                                              |
| [**PictureWidth**](-wia-iwiadispatchitem-picturewidth.md)<br/>       | Sola lettura<br/> | Larghezza, in pixel, delle immagini prodotte da questa fotocamera digitale. Si applica solo alle fotocamere digitali. <br/>                                                                                                                                               |
| [**ThumbHeight**](-wia-iwiadispatchitem-thumbheight.md)<br/>         | Sola lettura<br/> | Altezza, in pixel, dell'immagine di anteprima. Questa proprietà restituisce-1 se questo elemento non supporta le anteprime. <br/>                                                                                                                               |
| [**Anteprima**](-wia-iwiadispatchitem-thumbnail.md)<br/>             | Sola lettura<br/> | Percorso e nome del file dell'immagine di anteprima. Questa proprietà è **null** se l'elemento non supporta le anteprime o se non è possibile compilare un percorso. <br/>                                                                                                  |
| [**ThumbWidth**](-wia-iwiadispatchitem-thumbwidth.md)<br/>           | Sola lettura<br/> | Larghezza, in pixel, dell'immagine di anteprima. Questa proprietà restituisce-1 se questo elemento non supporta le anteprime. <br/>                                                                                                                                |
| [**Tempo**](-wia-iwiadispatchitem-time.md)<br/>                       | Sola lettura<br/> | Ora corrente. Si applica solo ai dispositivi. <br/>                                                                                                                                                                                                      |
| [**Larghezza**](-wia-iwiadispatchitem-width.md)<br/>                     | Sola lettura<br/> | Larghezza, in pixel, dell'elemento. <br/>                                                                                                                                                                                                              |



 

## <a name="remarks"></a>Commenti

### <a name="creationaccess-functions"></a>Funzioni di accesso per la creazione \\

Per recuperare un riferimento all'oggetto, utilizzare uno dei seguenti elementi:



[**TakePicture**](-wia-iwiadispatchitem-takepicture.md)

[**Creare**](-wia-iwiadeviceinfo-create.md)

[**Create**](-wia-iwia-create.md)



 

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 2000 Professional, \[ solo app desktop Windows XP\]<br/>                                        |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2003\]<br/>                                                          |
| DLL<br/>                      | <dl> <dt>Wiascr.dll (versione 4,90 o successiva)</dt> </dl> |



 

 




