---
description: L'azione RegisterProduct registra le informazioni sul prodotto con il programma di installazione e con Installazione applicazioni. Inoltre, questa azione archivia il pacchetto di database Windows Installer nel computer locale.
ms.assetid: 689b09c7-9c17-42f5-ba31-cf9c6252e453
title: Azione RegisterProduct
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 185b670b7a24c31e6dc5adb402cd6c557e2eba9eac3db5138744cd1e827113ad
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118375962"
---
# <a name="registerproduct-action"></a>Azione RegisterProduct

L'azione RegisterProduct registra le informazioni sul prodotto con il programma di installazione e con Installazione applicazioni. Inoltre, questa azione archivia il pacchetto di database Windows Installer nel computer locale.

L'azione RegisterProduct configura i controlli visualizzati da Installazione applicazioni in Pannello di controllo. Per altre informazioni, vedere [Configuring Add/Remove Programs with Windows Installer](configuring-add-remove-programs-with-windows-installer.md).

## <a name="sequence-restrictions"></a>Restrizioni relative alle sequenze

Non sono presenti restrizioni di sequenza.

## <a name="actiondata-messages"></a>Messaggi ActionData



| Campo | Descrizione dei dati dell'azione            |
|-------|---------------------------------------|
| \[1\] | Informazioni sul prodotto registrato. |



 

## <a name="remarks"></a>Commenti

L'azione RegisterProduct non viene eseguita durante l'installazione in un punto di installazione amministrativa.

 

 



