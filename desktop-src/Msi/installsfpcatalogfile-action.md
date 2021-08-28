---
description: L'azione InstallSFPCatalogFile installa i cataloghi usati da Windows per Windows Protezione file.
ms.assetid: 1c8253f1-ac7d-4346-a16e-887d16f521d9
title: Azione InstallSFPCatalogFile
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 75f3992a64e5e3150759fdbc2c8221e6bd8672a2c75e72343280fb3e552f3cae
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119787011"
---
# <a name="installsfpcatalogfile-action"></a>Azione InstallSFPCatalogFile

L'azione InstallSFPCatalogFile installa i cataloghi usati da Windows per Windows Protezione file. InstallSFPCatalogFile esegue query sulla tabella [Component](component-table.md), la tabella [File](file-table.md), la [tabella FileSFPCatalog](filesfpcatalog-table.md) e la tabella [SFPCatalog](sfpcatalog-table.md). I cataloghi vengono installati se sono associati a un file in un componente impostato per l'installazione locale o se sono associati a un file ripristinato in un componente installato localmente.

## <a name="sequence-restrictions"></a>Restrizioni relative alle sequenze

L'azione InstallSFPCatalogFile deve essere sequenziata prima [di InstallFiles](installfiles-action.md) e dopo [CostFinalize.](costfinalize-action.md)

## <a name="actiondata-messages"></a>Messaggi ActionData



| Campo | Descrizione dei dati dell'azione                                    |
|-------|---------------------------------------------------------------|
| \[1\] | Nome del catalogo da installare.                          |
| \[2\] | Nome del catalogo da cui dipende l'installazione del catalogo. |



 

## <a name="remarks"></a>Commenti

Catalogo che dipende da un altro catalogo installato dopo il catalogo padre.

 

 



