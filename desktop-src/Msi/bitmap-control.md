---
description: Il controllo Bitmap visualizza un file di immagine statica bitmap o JPEG. Il Windows installer determinerà automaticamente il formato dei dati binari e visualizza l'immagine. Il controllo non supporta l'animazione.
ms.assetid: 4b511d8a-1819-4a9b-a942-dc32fade75c6
title: Controllo Bitmap
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f677a7745d3920d5fee44cd64489f9f2c69f8cdb1fb697a0020046a92583e569
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120045231"
---
# <a name="bitmap-control"></a>Controllo Bitmap

Il controllo Bitmap visualizza un file di immagine statica bitmap o JPEG. Il Windows installer determinerà automaticamente il formato dei dati binari e visualizza l'immagine. Il controllo non supporta l'animazione.

**Windows 8 e Windows Server 2012:** Il file di immagine può essere in qualsiasi formato standard supportato da Windows Imaging Component (WIC), tra cui TIFF, JPEG, PNG, GIF, BMP e HDPhoto. Il controllo non supporta l'animazione.

## <a name="control-attributes"></a>Attributi del controllo

Con questo controllo è possibile usare gli attributi seguenti. Per modificare il valore di un attributo usando un evento , sottoscrivere il controllo a un oggetto ControlEvent nella tabella [EventMapping](eventmapping-table.md) ed elencare l'identificatore dell'attributo nella colonna Attribute . Immettere l'identificatore di ControlEvent nella colonna Event .



| Identificatore dell'attributo                                 | Bit esadecimale                  | Descrizione                                                                                                                                                                                                                                                                                                                                                                     |
|------------------------------------------------------|----------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Position](position-control-attribute.md)           |                                  | Posizione del controllo nella finestra di dialogo. Immettere la larghezza, l'altezza e le coordinate dell'angolo sinistro del controllo nelle colonne Width, Height, X e Y della [tabella Control](control-table.md) o [BBControl](bbcontrol-table.md). Usare le [unità del programma](installer-units.md) di installazione per lunghezza e distanza.<br/>                                         |
| [Text](text-control-attribute.md)                   |                                  | Contiene il nome di una bitmap archiviata nella [tabella binary](binary-table.md). Per visualizzare una bitmap archiviata nella tabella Binary, eseguire le operazioni seguenti. Immettere il nome dell'immagine bitmap visualizzata nella colonna Nome della tabella Binaria nella colonna Testo del record della tabella [Controllo](control-table.md) per questo controllo. <br/>                                         |
| [Visible](visible-control-attribute.md)             | 0x00000000 0x00000001<br/> | Controllo nascosto. Controllo visibile.<br/> Includere questo bit nella parola di bit della colonna Attributes nella tabella [Control](control-table.md) o [BBControl per](bbcontrol-table.md)rendere il controllo visibile o nascosto al momento della creazione.<br/> È anche possibile nascondere o visualizzare un controllo usando la [tabella ControlCondition](controlcondition-table.md).<br/> |
| [Sunken](sunken-control-attribute.md)               | 0x00000000 0x00000004<br/> | Visualizza lo stile di visualizzazione predefinito. Visualizza il controllo con un aspetto 3D incassato.<br/> Includere questi bit nella parola di bit nella colonna Attributi della [tabella Control](control-table.md).<br/>                                                                                                                                                                   |
| [Controllo FixedSize](fixedsize-control-attribute.md) | 0x00000000 0x00100000<br/> | Estende l'immagine bitmap per adattarla al controllo. Ritaglia o centra l'immagine bitmap nel controllo .<br/> Includere questo bit nella parola di bit della colonna Attributes della tabella [BBControl](bbcontrol-table.md) o [della tabella Control](control-table.md).<br/>                                                                                                       |



 

## <a name="remarks"></a>Commenti

Questo controllo può essere creato dalla classe STATIC usando la [**funzione CreateWindowEx.**](/windows/win32/api/winuser/nf-winuser-createwindowexa) Ha gli stili **SS \_ BITMAP,** **SS \_ CENTERIMAGE,** **WS \_ CHILD** e **WS \_ GROUP.**

 

