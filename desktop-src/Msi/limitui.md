---
description: Se la proprietà LIMITUI è impostata, il livello di interfaccia utente utilizzato durante l'installazione del pacchetto è limitato a Basic.
ms.assetid: 1a75e66b-958a-4fa8-b13c-ced976c9508e
title: Proprietà LIMITUI
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e564e82a2daba4b6d5a91cb05acd74e1efc26c84
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106325029"
---
# <a name="limitui-property"></a>Proprietà LIMITUI

Se la proprietà **LIMITUI** è impostata, il livello di interfaccia utente utilizzato durante l'installazione del pacchetto è limitato a Basic. Questa proprietà è obbligatoria nei pacchetti che non dispongono di un'interfaccia utente creata, ma che contengono ancora tabelle dell'interfaccia utente, ad esempio la [tabella della finestra di dialogo](dialog-table.md). Per una descrizione dei livelli dell'interfaccia utente, vedere [ **MsiSetInternalUI**](/windows/desktop/api/Msi/nf-msi-msisetinternalui)

## <a name="remarks"></a>Commenti

I pacchetti di installazione contenenti la proprietà **LIMITUI** devono anche contenere la proprietà [**ARPNOMODIFY**](arpnomodify.md) . Questa operazione è necessaria affinché un utente ottenga il comportamento corretto da **Installazione applicazioni** nell'utilità del **Pannello di controllo** quando si tenta di configurare un prodotto.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Versione<br/> | Windows Installer 5,0 in Windows Server 2012, Windows 8, Windows Server 2008 R2 o Windows 7. Windows Installer 4,0 o Windows Installer 4,5 in Windows Server 2008 o Windows Vista. Windows Installer in Windows Server 2003 o Windows XP. Vedere i [requisiti di Run-Time Windows Installer](windows-installer-portal.md) per informazioni sul Service Pack minimo di Windows richiesto da una versione Windows Installer.<br/> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Proprietà](properties.md)
</dt> <dt>

[**MsiSetInternalUI**](/windows/desktop/api/Msi/nf-msi-msisetinternalui)
</dt> <dt>

[**ARPNOMODIFY**](arpnomodify.md)
</dt> </dl>

 

 




