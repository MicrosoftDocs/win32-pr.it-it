---
description: Il programma di installazione imposta il valore della proprietà MsiPatchRemovalList su un elenco di patch che vengono rimosse durante l'installazione.
ms.assetid: 6e0b391a-d840-4f01-af12-4708ce6c9ce8
title: Proprietà MsiPatchRemovalList
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f2af522d9570297f2ff911b501bc543cf4b5971c
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106326267"
---
# <a name="msipatchremovallist-property"></a>Proprietà MsiPatchRemovalList

Il programma di installazione imposta il valore della proprietà **MsiPatchRemovalList** su un elenco di patch che vengono rimosse durante l'installazione. Le patch sono rappresentate nell'elenco in base ai relativi GUID di codice della patch separati da punti e virgola.

Gli sviluppatori possono utilizzare la proprietà **MsiPatchRemovalList** per creare un pacchetto di Windows Installer o una patch che esegue [azioni personalizzate](custom-actions.md) sulla rimozione di una patch. L'azione personalizzata può essere creata nel pacchetto di installazione originale, una patch che è già stata applicata al pacchetto o una patch che non è una [patch non installabile](uninstallable-patches.md). L'azione personalizzata può essere condizionata nella proprietà **MsiPatchRemovalList** delle tabelle di sequenza. Per ulteriori informazioni sulle azioni conditionalizing, vedere [utilizzo delle proprietà nelle istruzioni condizionali](using-properties-in-conditional-statements.md) .

L'azione personalizzata può ottenere i GUID delle patch da rimuovere dal valore della proprietà **MsiPatchRemovalList** . L'azione personalizzata può determinare se lo stato di installazione della patch è applicato, obsoleto o sostituito chiamando la funzione [**MsiGetPatchInfoEx**](/windows/desktop/api/Msi/nf-msi-msigetpatchinfoexa) o la proprietà [**PatchProperty**](patch-patchproperty.md) dell' [oggetto patch](patch-object.md).

## <a name="remarks"></a>Commenti

Per ulteriori informazioni sulla rimozione di patch, vedere [rimozione di patch](removing-patches.md).

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Versione<br/> | Windows Installer 5,0 in Windows Server 2012, Windows 8, Windows Server 2008 R2 o Windows 7. Windows Installer 4,0 o Windows Installer 4,5 in Windows Server 2008 o Windows Vista. Windows Installer 3,0 o versioni successive in Windows Server 2003 o Windows XP. Vedere i [requisiti di Run-Time Windows Installer](windows-installer-portal.md) per informazioni sul Service Pack minimo di Windows richiesto da una versione Windows Installer.<br/> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Proprietà](properties.md)
</dt> <dt>

[Non supportato in Windows Installer 2,0 e versioni precedenti](not-supported-in-windows-installer-version-2-0.md)
</dt> </dl>

 

 




