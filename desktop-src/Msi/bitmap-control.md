---
description: Il controllo bitmap Visualizza una bitmap o un file di immagine statica JPEG. Il Windows Installer determinerà automaticamente il formato dei dati binari e visualizzerà l'immagine. Il controllo non supporta l'animazione.
ms.assetid: 4b511d8a-1819-4a9b-a942-dc32fade75c6
title: Controllo bitmap
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 058b67d52266906735719976bf7311b4f562b474
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106311012"
---
# <a name="bitmap-control"></a>Controllo bitmap

Il controllo bitmap Visualizza una bitmap o un file di immagine statica JPEG. Il Windows Installer determinerà automaticamente il formato dei dati binari e visualizzerà l'immagine. Il controllo non supporta l'animazione.

**Windows 8 e Windows Server 2012:** Il file di immagine può essere in qualsiasi formato standard supportato da Windows Imaging Component (WIC), inclusi TIFF, JPEG, PNG, GIF, BMP e HDPhoto. Il controllo non supporta l'animazione.

## <a name="control-attributes"></a>Attributi del controllo

Con questo controllo è possibile usare gli attributi seguenti. Per modificare il valore di un attributo utilizzando un evento, sottoscrivere il controllo in un ControlEvent nella [tabella EventMapping](eventmapping-table.md) ed elencare l'identificatore dell'attributo nella colonna attributo. Immettere l'identificatore del ControlEvent nella colonna evento.



| Identificatore di attributo                                 | Bit esadecimale                  | Descrizione                                                                                                                                                                                                                                                                                                                                                                     |
|------------------------------------------------------|----------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Position](position-control-attribute.md)           |                                  | Posizione del controllo nella finestra di dialogo. Immettere la larghezza, l'altezza e le coordinate del controllo dell'angolo sinistro del controllo nelle colonne Width, Height, X e Y della [tabella di controllo](control-table.md) o della [tabella BBControl](bbcontrol-table.md). Usare le [unità del programma di installazione](installer-units.md) per lunghezza e distanza.<br/>                                         |
| [Text](text-control-attribute.md)                   |                                  | Contiene il nome di una bitmap archiviata nella [tabella binaria](binary-table.md). Per visualizzare una bitmap archiviata nella tabella binaria, effettuare le operazioni seguenti. Immettere il nome dell'immagine bitmap visualizzata nella colonna nome della tabella binaria nella colonna di testo del record della tabella dei [controlli](control-table.md) per questo controllo. <br/>                                         |
| [Visible](visible-control-attribute.md)             | 0x00000001 0x00000000<br/> | Controllo nascosto. Controllo visibile.<br/> Includere questo bit nella parola bit della colonna attributi nella [tabella dei controlli](control-table.md) o nella [tabella BBControl](bbcontrol-table.md). per rendere il controllo visibile o nascosto alla sua creazione.<br/> È anche possibile nascondere o visualizzare un controllo usando la [tabella ControlCondition](controlcondition-table.md).<br/> |
| [Sunken](sunken-control-attribute.md)               | 0x00000004 0x00000000<br/> | Visualizza lo stile di visualizzazione predefinito. Visualizza il controllo con un aspetto incassato, 3D.<br/> Includere questi bit nella parola bit nella colonna attributi della [tabella dei controlli](control-table.md).<br/>                                                                                                                                                                   |
| [Controllo FixedSize](fixedsize-control-attribute.md) | 0x00100000 0x00000000<br/> | Estende l'immagine bitmap per adattarla al controllo. Coltiva o Centra l'immagine bitmap nel controllo.<br/> Includere questo bit nella parola bit della colonna Attributes della [tabella BBControl](bbcontrol-table.md) o della tabella dei [controlli](control-table.md).<br/>                                                                                                       |



 

## <a name="remarks"></a>Commenti

Questo controllo può essere creato dalla classe statica tramite la funzione [**CreateWindowEx**](/windows/win32/api/winuser/nf-winuser-createwindowexa) . Dispone degli stili **\_ bitmap SS**, **SS \_ CENTERIMAGE**, **WS \_ child** e **WS \_ Group** .

 

