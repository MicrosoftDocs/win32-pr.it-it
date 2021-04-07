---
description: In un volume file system NTFS ogni file e directory dispone di un attributo di compressione.
ms.assetid: 8aca120c-22a7-4dc8-a921-dfcec1277452
title: Attributo Compression
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d2e8e86eebe919476851f35f77cf10d6a07035d1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "103885737"
---
# <a name="compression-attribute"></a>Attributo Compression

In un volume file system NTFS ogni file e directory dispone di un *attributo di compressione*. Altri file System possono implementare anche un attributo di compressione per singoli file e directory.

È possibile determinare se un file system supporta un attributo di compressione per file e directory chiamando la funzione [**GetVolumeInformation**](/windows/desktop/api/FileAPI/nf-fileapi-getvolumeinformationa) ed esaminando il flag di bit di **\_ \_ compressione del file di file** .

Utilizzare la funzione [**GetFileAttributes**](/windows/desktop/api/FileAPI/nf-fileapi-getfileattributesa) o [**GetFileAttributesEx**](/windows/desktop/api/FileAPI/nf-fileapi-getfileattributesexa) per determinare l'attributo di compressione di un file o di una directory.

Se è impostato l'attributo di compressione di un file (**\_ attributo file \_ compresso**), tutti i dati nel file vengono compressi. Se l'attributo è chiaro, nessuno dei dati nel file viene compresso. Non esiste alcuno stato parzialmente compresso da un punto di vista della programmazione in modalità utente; l'attributo Compression è un semplice indicatore booleano dello stato di compressione.

L'attributo di compressione di una directory fornisce un attributo di compressione predefinito per i file e le sottodirectory appena creati. Quando si chiama [**CreateFile**](/windows/desktop/api/FileAPI/nf-fileapi-createfilea) o [**CreateDirectory**](/windows/desktop/api/FileAPI/nf-fileapi-createdirectorya) per creare un nuovo file o una nuova directory, il nuovo file o la nuova directory eredita l'attributo di compressione della relativa directory padre.

Per modificare l' **attributo \_ \_ compresso dell'attributo file** per un file o una directory, è necessario usare la funzione [**DeviceIoControl**](/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol) con il codice di controllo della [**\_ \_ compressione FSCTL set**](/windows/win32/api/winioctl/ni-winioctl-fsctl_set_compression) .

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**Costanti di attributi file**](file-attribute-constants.md)
</dt> </dl>

 

 
