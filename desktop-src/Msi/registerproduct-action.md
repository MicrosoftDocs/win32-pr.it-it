---
description: L'azione RegisterProduct registra le informazioni sul prodotto con il programma di installazione e con installazione applicazioni. Questa azione archivia inoltre il pacchetto di database Windows Installer nel computer locale.
ms.assetid: 689b09c7-9c17-42f5-ba31-cf9c6252e453
title: Azione RegisterProduct
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5afa2d3e9f00f736b8c4c7864d8ec4baa3aa8ad9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106311708"
---
# <a name="registerproduct-action"></a>Azione RegisterProduct

L'azione RegisterProduct registra le informazioni sul prodotto con il programma di installazione e con installazione applicazioni. Questa azione archivia inoltre il pacchetto di database Windows Installer nel computer locale.

L'azione RegisterProduct configura i controlli visualizzati da installazione applicazioni nel pannello di controllo. Per ulteriori informazioni, vedere [configurazione di installazione applicazioni con Windows Installer](configuring-add-remove-programs-with-windows-installer.md).

## <a name="sequence-restrictions"></a>Restrizioni sequenza

Non esistono restrizioni di sequenza.

## <a name="actiondata-messages"></a>Messaggi ActionData



| Campo | Descrizione dei dati dell'azione            |
|-------|---------------------------------------|
| \[1\] | Informazioni sul prodotto registrato. |



 

## <a name="remarks"></a>Commenti

L'azione RegisterProduct non viene eseguita durante l'installazione in un punto di installazione amministrativa.

 

 



