---
description: Il programma di installazione imposta il valore della proprietà MsiPatchRemovalList su un elenco di patch che vengono rimosse durante l'installazione.
ms.assetid: 6e0b391a-d840-4f01-af12-4708ce6c9ce8
title: MsiPatchRemovalList - proprietà
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 93df2cdfc658875526c049ca7503e66a5c318df896a604a82c18751ac3358285
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119065981"
---
# <a name="msipatchremovallist-property"></a>MsiPatchRemovalList - proprietà

Il programma di installazione imposta il valore della **proprietà MsiPatchRemovalList** su un elenco di patch che vengono rimosse durante l'installazione. Le patch sono rappresentate nell'elenco dai RELATIVI GUID del codice di patch separati da punti e virgola.

Gli sviluppatori possono usare la proprietà **MsiPatchRemovalList** per creare un [](custom-actions.md) pacchetto o una patch del programma di installazione di Windows che esegue azioni personalizzate sulla rimozione di una patch. È possibile creare l'azione personalizzata nel pacchetto di installazione originale, in una patch già applicata al pacchetto o in una patch non [disinstallabile.](uninstallable-patches.md) L'azione personalizzata può essere condizionale nella **proprietà MsiPatchRemovalList** nelle tabelle di sequenza. Per [altre informazioni sulle azioni condizionali,](using-properties-in-conditional-statements.md) vedere Uso delle proprietà nelle istruzioni condizionali.

L'azione personalizzata può ottenere i GUID delle patch rimosse dal valore della **proprietà MsiPatchRemovalList.** L'azione personalizzata può determinare se lo stato di installazione della patch viene applicato, obsoleto o sostituito chiamando la funzione [**MsiGetPatchInfoEx**](/windows/desktop/api/Msi/nf-msi-msigetpatchinfoexa) o la proprietà [**PatchProperty**](patch-patchproperty.md) dell'oggetto [Patch](patch-object.md).

## <a name="remarks"></a>Commenti

Per altre informazioni sulla rimozione delle patch, vedere [Rimozione di patch.](removing-patches.md)

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Versione<br/> | Windows Programma di installazione 5.0 Windows Server 2012, Windows 8, Windows Server 2008 R2 o Windows 7. Windows Installer 4.0 o Windows Installer 4.5 in Windows Server 2008 o Windows Vista. Windows Programma di installazione 3.0 o versione successiva in Windows Server 2003 o Windows XP. Per informazioni [Windows service](windows-installer-portal.md) pack minimo necessario per Run-Time versione del programma di installazione di Windows, vedere i requisiti minimi Windows Service Pack.<br/> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Proprietà](properties.md)
</dt> <dt>

[Non supportato in Windows Installer 2.0 e versioni precedenti](not-supported-in-windows-installer-version-2-0.md)
</dt> </dl>

 

 




