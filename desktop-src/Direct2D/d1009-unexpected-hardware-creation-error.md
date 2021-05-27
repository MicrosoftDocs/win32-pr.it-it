---
title: D1009 Errore di creazione hardware imprevisto
description: Si è verificato un errore imprevisto \ errore\ durante il tentativo di creare una destinazione Direct3D.
ms.assetid: 1ff34b1f-0ab3-4821-97f5-a4e67831383a
keywords:
- D1009 Errore imprevisto di creazione dell'hardware Direct2D
topic_type:
- apiref
api_name:
- D1009 Unexpected Hardware Creation Error
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fa51d2536995feb51081134e412d94617f34d069
ms.sourcegitcommit: f848119a8faa29b27585f4df53f6e50ee9666684
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 05/27/2021
ms.locfileid: "110548716"
---
# <a name="d1009-unexpected-hardware-creation-error"></a>D1009: Errore imprevisto di creazione dell'hardware

Si è verificato \[ *un errore* \] imprevisto durante il tentativo di creare una destinazione Direct3D.

## <a name="placeholders"></a>Segnaposto

<dl> <dt>

<span id="error"></span><span id="ERROR"></span>*Errore*
</dt> <dd>

Numero di errore.

</dd> </dl> 

| &nbsp;      |  &nbsp; |
|-------------|---------|
| Livello di errore | Avviso |



 

## <a name="possible-causes"></a>Possibili cause

-   La destinazione è maggiore delle dimensioni massime della bitmap.
-   Memoria video insufficiente durante la creazione della destinazione di rendering.
-   Non è stato possibile creare alcun dispositivo Direct3D.
-   L'applicazione è in esecuzione in IA64.

 

 




