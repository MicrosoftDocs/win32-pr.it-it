---
description: In un volume file system NTFS, ogni file e directory ha un attributo di compressione.
ms.assetid: 8aca120c-22a7-4dc8-a921-dfcec1277452
title: Attributo di compressione
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 99fb42aaa30fc3e5d2ef36da85bae194950c587d024510b18233f3c83504ab88
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119982151"
---
# <a name="compression-attribute"></a>Attributo di compressione

In un volume file system NTFS, ogni file e directory ha un attributo *di compressione*. Altri file system possono anche implementare un attributo di compressione per singoli file e directory.

È possibile determinare se file system supporta un attributo di compressione per file e directory chiamando la [**funzione GetVolumeInformation**](/windows/desktop/api/FileAPI/nf-fileapi-getvolumeinformationa) ed esaminando il flag di bit **FILE FILE \_ \_ COMPRESSION.**

Usare la [**funzione GetFileAttributes**](/windows/desktop/api/FileAPI/nf-fileapi-getfileattributesa) o [**GetFileAttributesEx**](/windows/desktop/api/FileAPI/nf-fileapi-getfileattributesexa) per determinare l'attributo di compressione di un file o di una directory.

Se l'attributo di compressione di un file è impostato **(FILE \_ ATTRIBUTE \_ COMPRESSED),** tutti i dati nel file vengono compressi. Se l'attributo è chiaro, nessuno dei dati nel file viene compresso. Non esiste uno stato parzialmente compresso dal punto di vista della programmazione in modalità utente. L'attributo di compressione è un indicatore booleano semplice dello stato di compressione.

L'attributo di compressione di una directory fornisce un attributo di compressione predefinito per i file e le sottodirectory appena creati. Quando si chiama [**CreateFile**](/windows/desktop/api/FileAPI/nf-fileapi-createfilea) o [**CreateDirectory**](/windows/desktop/api/FileAPI/nf-fileapi-createdirectorya) per creare un nuovo file o directory, il nuovo file o directory eredita l'attributo di compressione della directory padre.

Per modificare **l'attributo FILE \_ ATTRIBUTE \_ COMPRESSED** per un file o una directory, è necessario usare la funzione [**DeviceIoControl**](/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol) con il codice di controllo [**FSCTL \_ SET \_ COMPRESSION.**](/windows/win32/api/winioctl/ni-winioctl-fsctl_set_compression)

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**Costanti di attributi file**](file-attribute-constants.md)
</dt> </dl>

 

 
