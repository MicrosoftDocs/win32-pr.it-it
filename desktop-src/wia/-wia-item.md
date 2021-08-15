---
description: Windows I dispositivi hardware WIA (Image Acquisition) sono rappresentati come alberi gerarchici di oggetti Item. L'elemento radice in questo albero rappresenta il dispositivo stesso, mentre gli elementi figlio rappresentano immagini, cartelle o scansioni.
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
ms.openlocfilehash: 2b5b32603f334148fede3bc2866367817fd3dcd5ab33aaa40bab84fe3cf49624
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118208934"
---
# <a name="item-object"></a>Oggetto Item

Windows I dispositivi hardware WIA (Image Acquisition) sono rappresentati come alberi gerarchici di **oggetti Item.** L'elemento radice in questo albero rappresenta il dispositivo stesso, mentre gli elementi figlio rappresentano immagini, cartelle o scansioni.

Usare **l'oggetto Item** per trasferire dati in un file, per esplorare l'albero degli elementi per un particolare dispositivo o per recuperare informazioni su un'immagine o un dispositivo.

## <a name="members"></a>Membri

**L'oggetto Item** ha questi tipi di membri:

-   [Metodi](#methods)
-   [Proprietà](#properties)

### <a name="methods"></a>Metodi

**L'oggetto Item** dispone di questi metodi.



| Metodo                                                         | Descrizione                                                                                                                                                                                                                                                                    |
|:---------------------------------------------------------------|:-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**GetItemsFromUI**](-wia-iwiadispatchitem-getitemsfromui.md) | Il [**metodo GetItemsFromUI**](-wia-iwiadispatchitem-getitemsfromui.md) dell'oggetto **Item** visualizza una finestra di dialogo che consente a un utente di selezionare immagini e audio da trasferire da un dispositivo.<br/>                                                                     |
| [**GetPropById**](-wia-iwiadispatchitem-getpropbyid.md)       | Il [**metodo GetPropById**](-wia-iwiadispatchitem-getpropbyid.md) dell'oggetto **Item** usa l'ID di una proprietà dell'elemento per restituirne il valore.<br/>                                                                                                                     |
| [**TakePicture**](-wia-iwiadispatchitem-takepicture.md)       | Il [**metodo TakePicture**](-wia-iwiadispatchitem-takepicture.md) dell'oggetto **Item** consente a un dispositivo fotocamera digitale di scattare una foto e restituisce un **oggetto Item** che rappresenta l'immagine risultante. Questo metodo si applica solo ai dispositivi con fotocamera digitale.<br/> |
| [**Trasferire**](-wia-iwiadispatchitem-transfer.md)             | Il [**metodo Transfer**](-wia-iwiadispatchitem-transfer.md) dell'oggetto **Item** trasferisce i dati da un dispositivo a un file. Questo metodo si applica solo agli elementi di tipo dispositivo.<br/>                                                                                         |



 

### <a name="properties"></a>Proprietà

**L'oggetto Item** ha queste proprietà.



| Proprietà                                                                    | Tipo di accesso          | Descrizione                                                                                                                                                                                                                                                 |
|:----------------------------------------------------------------------------|:---------------------|:------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Children**](-wia-iwiadispatchitem-children.md)<br/>               | Sola lettura<br/> | La [**proprietà Children**](-wia-iwiadispatchitem-children.md) dell'oggetto **Item** recupera una raccolta di **oggetti Item.** Gli elementi di questa raccolta rappresentano elementi che sono figli diretti di questo elemento nell'albero gerarchico. <br/> |
| [**ConnectStatus**](-wia-iwiadispatchitem-connectstatus.md)<br/>     | Sola lettura<br/> | Recupera lo stato di connessione del dispositivo. Questa proprietà si applica solo agli elementi di tipo dispositivo (elementi radice). I valori possibili sono "connected", "disconnected" o **NULL** (se questa proprietà non si applica all'elemento). <br/>                     |
| [**FirmwareVersion**](-wia-iwiadispatchitem-firmwareversion.md)<br/> | Sola lettura<br/> | Recupera la versione del firmware del dispositivo. Questa proprietà si applica solo agli elementi di tipo dispositivo (elementi radice). <br/>                                                                                                                                  |
| [**Fullname**](-wia-iwiadispatchitem-fullname.md)<br/>               | Sola lettura<br/> | Recupera il nome completo dell'elemento così come viene visualizzato nell'interfaccia utente. <br/>                                                                                                                                                                                    |
| [**Altezza**](-wia-iwiadispatchitem-height.md)<br/>                   | Sola lettura<br/> | Altezza, in pixel, dell'elemento. <br/>                                                                                                                                                                                                             |
| [**Itemtype**](-wia-iwiadispatchitem-itemtype.md)<br/>               | Sola lettura<br/> | Tipo di questo elemento. <br/>                                                                                                                                                                                                                          |
| [**Nome**](-wia-iwiadispatchitem-name.md)<br/>                       | Sola lettura<br/> | Nome dell'elemento così come viene visualizzato nell'interfaccia utente. <br/>                                                                                                                                                                                                   |
| [**PictureHeight**](-wia-iwiadispatchitem-pictureheight.md)<br/>     | Sola lettura<br/> | Altezza, in pixel, delle immagini prodotte dalla fotocamera digitale. Si applica solo alle fotocamere digitali. <br/>                                                                                                                                              |
| [**Proprietà PictureWidth**](-wia-iwiadispatchitem-picturewidth.md)<br/>       | Sola lettura<br/> | Larghezza, in pixel, delle immagini prodotte dalla fotocamera digitale. Si applica solo alle fotocamere digitali. <br/>                                                                                                                                               |
| [**ThumbHeight**](-wia-iwiadispatchitem-thumbheight.md)<br/>         | Sola lettura<br/> | Altezza, in pixel, dell'immagine di anteprima. Questa proprietà restituisce -1 se questo elemento non supporta le anteprime. <br/>                                                                                                                               |
| [**Anteprima**](-wia-iwiadispatchitem-thumbnail.md)<br/>             | Sola lettura<br/> | Percorso e nome file dell'immagine di anteprima. Questa proprietà è **NULL** se l'elemento non supporta le anteprime o se non è possibile determinare un percorso. <br/>                                                                                                  |
| [**ThumbWidth**](-wia-iwiadispatchitem-thumbwidth.md)<br/>           | Sola lettura<br/> | Larghezza, in pixel, dell'immagine di anteprima. Questa proprietà restituisce -1 se questo elemento non supporta le anteprime. <br/>                                                                                                                                |
| [**Ora**](-wia-iwiadispatchitem-time.md)<br/>                       | Sola lettura<br/> | Ora corrente. Si applica solo ai dispositivi. <br/>                                                                                                                                                                                                      |
| [**Larghezza**](-wia-iwiadispatchitem-width.md)<br/>                     | Sola lettura<br/> | Larghezza, in pixel, dell'elemento. <br/>                                                                                                                                                                                                              |



 

## <a name="remarks"></a>Commenti

### <a name="creationaccess-functions"></a>Creazione di \\ funzioni di accesso

Usare uno degli elementi seguenti per recuperare un riferimento all'oggetto :



[**TakePicture**](-wia-iwiadispatchitem-takepicture.md)

[**Crea**](-wia-iwiadeviceinfo-create.md)

[**Create**](-wia-iwia-create.md)



 

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 2000 Professional, Windows solo app desktop XP \[\]<br/>                                        |
| Server minimo supportato<br/> | Windows Solo app desktop di Server 2003 \[\]<br/>                                                          |
| DLL<br/>                      | <dl> <dt>Wiascr.dll (versione 4.90 o successiva)</dt> </dl> |



 

 




