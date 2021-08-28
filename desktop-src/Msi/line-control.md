---
description: Il controllo Line è una linea orizzontale.
ms.assetid: 8b180b71-1e80-47c0-bb44-d5fcecabaed2
title: Controllo Line
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7eb4dc02db9c701c0c5156a0e3f3e15a039893bae290fc7e8bee7dfce64f2eb7
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119763491"
---
# <a name="line-control"></a>Controllo Line

Il controllo Line è una linea orizzontale.

## <a name="control-attributes"></a>Attributi del controllo

Con questo controllo è possibile usare gli attributi seguenti. Per modificare il valore di un attributo usando un evento, sottoscrivere il controllo a un ControlEvent nella tabella [EventMapping](eventmapping-table.md) ed elencare l'identificatore dell'attributo nella colonna Attribute. Immettere l'identificatore di ControlEvent nella colonna Evento.



| Identificatore dell'attributo                       | Bit esadecimale                  | Descrizione                                                                                                                                                                                                                                                                                                                                                                     |
|--------------------------------------------|----------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Position](position-control-attribute.md) |                                  | Posizione del controllo nella finestra di dialogo. Immettere la larghezza, l'altezza e le coordinate dell'angolo sinistro del controllo nelle colonne Width, Height, X e Y della tabella [Control](control-table.md) o [BBControl](bbcontrol-table.md). Usare le [unità di installazione](installer-units.md) per lunghezza e distanza.<br/>                                         |
| [Visible](visible-control-attribute.md)   | 0x00000000 0x00000001<br/> | Controllo nascosto. Controllo visibile.<br/> Includere questo bit nella parola di bit della colonna Attributes nella tabella [Control](control-table.md) o [BBControl](bbcontrol-table.md) per rendere il controllo visibile o nascosto al momento della creazione.<br/> È anche possibile nascondere o visualizzare un controllo usando la [tabella ControlCondition](controlcondition-table.md).<br/> |
| [Sunken](sunken-control-attribute.md)     | 0x00000000 0x00000004<br/> | Visualizza lo stile di visualizzazione predefinito. Visualizza il controllo con un aspetto 3D incassato.<br/> Includere questi bit nella parola di bit nella colonna Attributi della [tabella Control](control-table.md).<br/>                                                                                                                                                                   |



 

## <a name="remarks"></a>Commenti

Questo controllo può essere creato dalla classe STATIC usando la [**funzione CreateWindowEx.**](/windows/win32/api/winuser/nf-winuser-createwindowexa) Ha gli **stili SS \_ ETCHEDHORZ** **e SS \_ SUNKEN.**

 

 
