---
description: L'azione InstallSFPCatalogFile installa i cataloghi usati da Windows me per la protezione dei file di Windows.
ms.assetid: 1c8253f1-ac7d-4346-a16e-887d16f521d9
title: Azione InstallSFPCatalogFile
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ddc4192f8ee0062c51833292a98c28ea27c12531
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106305965"
---
# <a name="installsfpcatalogfile-action"></a>Azione InstallSFPCatalogFile

L'azione InstallSFPCatalogFile installa i cataloghi usati da Windows me per la protezione dei file di Windows. InstallSFPCatalogFile esegue una query sulla tabella dei [componenti](component-table.md), sulla tabella [file](file-table.md), sulla tabella [FileSFPCatalog](filesfpcatalog-table.md) e sulla [tabella SFPCatalog](sfpcatalog-table.md). I cataloghi vengono installati se sono associati a un file in un componente impostato per l'installazione locale o se sono associati a un file da ripristinare in un componente installato localmente.

## <a name="sequence-restrictions"></a>Restrizioni sequenza

L'azione InstallSFPCatalogFile deve essere sequenziata prima di [InstallFiles](installfiles-action.md) e dopo [CostFinalize secondo](costfinalize-action.md).

## <a name="actiondata-messages"></a>Messaggi ActionData



| Campo | Descrizione dei dati dell'azione                                    |
|-------|---------------------------------------------------------------|
| \[1\] | Nome del catalogo da installare.                          |
| \[2\] | Nome del catalogo da cui dipende l'installazione di questo catalogo. |



 

## <a name="remarks"></a>Commenti

Catalogo che dipende da un altro catalogo installato dopo il catalogo padre.

 

 



