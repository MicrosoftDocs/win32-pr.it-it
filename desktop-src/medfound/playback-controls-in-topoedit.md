---
description: Controlli di riproduzione in TopoEdit
ms.assetid: 36ebfa9e-7092-4a93-b633-8eefef8ac9e6
title: Controlli di riproduzione in TopoEdit
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 174317fbf53dc6d2573414c60d5d4cde1a010f95
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104566412"
---
# <a name="playback-controls-in-topoedit"></a>Controlli di riproduzione in TopoEdit

Dopo la risoluzione, una topologia viene accodata nella sessione multimediale per la riproduzione. TopoEdit fornisce il controllo di trasporto per la modifica dello stato della topologia nella sessione multimediale.

La tabella seguente illustra il comando menu/barra degli strumenti e il metodo Media Foundation equivalente per ogni operazione.



| Comando menu/barra degli strumenti                                                                                                                                                                                                                          | Metodo Media Foundation                                 |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------|
| Scegliere **Riproduci** dal menu **controlli** . \[ nuova riga \] o \[ nuova riga \] fare clic sul pulsante **Riproduci** sulla barra degli strumenti (mostrata nella figura seguente). \[ \] ![ schermata di nuova riga del pulsante Riproduci](images/536e8908-ef44-4d25-98f1-c06b5ef37591.jpg)    | [**IMFMediaSession:: Start**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-start) |
| Scegliere **Interrompi** dal menu **controlli** . \[ nuova riga \] o \[ nuova riga \] fare clic sul pulsante **Arresta** sulla barra degli strumenti (mostrata nella figura seguente). \[ Screenshot di nuova riga \] ![ del pulsante Interrompi](images/f74657f8-12b3-414a-a1f1-39b7ae2b20f1.jpg)    | [**IMFMediaSession:: Stop**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-stop)   |
| Scegliere **Sospendi** dal menu **controlli** . \[ nuova riga \] o \[ nuova riga \] fare clic sul pulsante **Sospendi** sulla barra degli strumenti (mostrata nella figura seguente). \[ Screenshot di nuova riga \] ![ del pulsante Sospendi](images/156351f1-7215-4062-b4a1-0a0aaa79d205.jpg) | [**IMFMediaSession::P ause**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-pause) |



 

Per informazioni sul controllo della riproduzione a livello di programmazione tramite le API di Media Foundation, vedere [How to Control Presentation States](how-to-control-presentation-states.md).

## <a name="seeking"></a>La ricerca

Se la topologia è ricercabile, è possibile cercare usando la barra di ricerca (mostrata nella figura seguente) per specificare una posizione nella sequenza temporale della topologia per iniziare la riproduzione.

![screenshot della barra di ricerca](images/95a4e3ef-8489-4e26-9f02-436f81d8a96e.jpg)

> [!Note]  
> Se l'origine del supporto è ricercabile, il comando Stop Cerca anche la topologia all'inizio del flusso.

 

## <a name="changing-the-playback-rate"></a>Modifica della velocità di riproduzione

Se l'origine multimediale sottostante per la topologia supporta più frequenze di riproduzione, è possibile usare la barra della velocità per modificare la velocità di riproduzione. Per eseguire rapidamente il provisioning di una topologia nella sessione multimediale, aumentare la velocità trascinando il dispositivo di scorrimento a destra, come illustrato nella figura seguente.

![screenshot della barra della velocità](images/6e094ecf-c87f-4f27-bca7-a53cc790f5c2.jpg)

> [!Note]  
> In questa versione, TopoEdit supporta solo frequenze positive. La riproduzione inversa non è supportata.

 

Per informazioni sulla modifica della velocità di riproduzione a livello di codice usando le API di Media Foundation, vedere [informazioni sul controllo della frequenza](about-rate-control.md).

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Menu TopoEdit](topoedit-menus.md)
</dt> <dt>

[Barra degli strumenti TopoEdit](topoedit-toolbar.md)
</dt> <dt>

[TopoEdit](topoedit.md)
</dt> </dl>

 

 



