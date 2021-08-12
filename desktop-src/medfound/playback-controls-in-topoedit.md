---
description: Controlli di riproduzione in TopoModifica
ms.assetid: 36ebfa9e-7092-4a93-b633-8eefef8ac9e6
title: Controlli di riproduzione in TopoModifica
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 10c59dfceb30f839ba58d37385a3178d42429eb858c98f3f5196dd95141ac2a2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118239691"
---
# <a name="playback-controls-in-topoedit"></a>Controlli di riproduzione in TopoModifica

Una volta risolta, una topologia viene accodata nella sessione multimediale per la riproduzione. TopoEdit fornisce il controllo del trasporto per la modifica dello stato della topologia nella sessione multimediale.

La tabella seguente illustra il comando di menu/barra degli strumenti e il metodo Media Foundation per ogni operazione.



| Comando menu/barra degli strumenti                                                                                                                                                                                                                          | metodo Media Foundation                                 |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------|
| Scegliere **Riproduci** dal menu **Controlli**. \[ newline -oppure- newline fare clic sul pulsante play sulla barra degli strumenti \] \[ \] (illustrato nell'immagine seguente).  \[ Screenshot di \] ![ nuova riga del pulsante di riproduzione](images/536e8908-ef44-4d25-98f1-c06b5ef37591.jpg)    | [**IMFMediaSession::Start**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-start) |
| Scegliere **Arresta** dal menu **Controlli**. \[ newline \] -oppure- newline fare clic sul pulsante stop sulla barra degli \[ strumenti \] (illustrato nell'immagine seguente).  \[ Screenshot di \] ![ nuova riga del pulsante di arresto](images/f74657f8-12b3-414a-a1f1-39b7ae2b20f1.jpg)    | [**IMFMediaSession::Stop**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-stop)   |
| Scegliere **Sospendi** dal menu **Controlli**. \[ newline \] -oppure- newline fare clic sul pulsante sospendi sulla \[ barra degli strumenti \] (illustrato nell'immagine seguente).  \[ Screenshot di \] ![ nuova riga del pulsante di sospensione](images/156351f1-7215-4062-b4a1-0a0aaa79d205.jpg) | [**IMFMediaSession::P ause**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-pause) |



 

Per informazioni sul controllo della riproduzione a livello di codice usando Media Foundation API, vedere [Come controllare gli stati di presentazione.](how-to-control-presentation-states.md)

## <a name="seeking"></a>riercare

Se la topologia è ricercabile, è possibile cercare usando la barra di ricerca (illustrata nell'immagine seguente) per specificare una posizione nella sequenza temporale della topologia per avviare la riproduzione.

![Screenshot della barra di ricerca](images/95a4e3ef-8489-4e26-9f02-436f81d8a96e.jpg)

> [!Note]  
> Se l'origine multimediale è ricercabile, il comando Arresta cerca anche la topologia all'inizio del flusso.

 

## <a name="changing-the-playback-rate"></a>Modifica della velocità di riproduzione

Se l'origine multimediale sottostante per la topologia supporta più frequenze di riproduzione, è possibile usare la barra della frequenza per modificare la velocità di riproduzione. Per inoltrare rapidamente una topologia nella sessione multimediale, aumentare la velocità trascinando il dispositivo di scorrimento verso destra, come illustrato nell'immagine seguente.

![Screenshot della barra della frequenza](images/6e094ecf-c87f-4f27-bca7-a53cc790f5c2.jpg)

> [!Note]  
> In questa versione, TopoEdit supporta solo percentuali positive. La riproduzione inversa non è supportata.

 

Per informazioni sulla modifica della frequenza di riproduzione a livello di codice usando Media Foundation API, vedere [Informazioni sul controllo della frequenza.](about-rate-control.md)

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Menu TopoEdit](topoedit-menus.md)
</dt> <dt>

[Barra degli strumenti TopoEdit](topoedit-toolbar.md)
</dt> <dt>

[TopoModifica](topoedit.md)
</dt> </dl>

 

 



