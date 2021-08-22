---
description: Se la proprietà LIMITUI è impostata, il livello dell'interfaccia utente usato durante l'installazione del pacchetto è limitato a Basic.
ms.assetid: 1a75e66b-958a-4fa8-b13c-ced976c9508e
title: LIMITUI - proprietà
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 969b6e1c1de5a55581fa8d24f6d538c829e18fb48afb9bdc2fd04bae69c15162
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119013139"
---
# <a name="limitui-property"></a>LIMITUI - proprietà

Se la **proprietà LIMITUI** è impostata, il livello dell'interfaccia utente usato durante l'installazione del pacchetto è limitato a Basic. Questa proprietà è obbligatoria nei pacchetti che non dispongono di un'interfaccia utente ma che contengono ancora tabelle dell'interfaccia utente, ad esempio la [tabella Dialog](dialog-table.md). Per una descrizione dei livelli dell'interfaccia utente, [ **vedere MsiSetInternalUI**](/windows/desktop/api/Msi/nf-msi-msisetinternalui)

## <a name="remarks"></a>Commenti

I pacchetti di installazione **contenenti la proprietà LIMITUI** devono contenere anche [**la proprietà ARPNOMODIFY.**](arpnomodify.md) Questo è necessario per un utente per  ottenere il comportamento corretto da Installazione applicazioni nell'utilità **Pannello di controllo** quando si tenta di configurare un prodotto.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Versione<br/> | Windows Programma di installazione 5.0 Windows Server 2012, Windows 8, Windows Server 2008 R2 o Windows 7. Windows Installer 4.0 o Windows Installer 4.5 in Windows Server 2008 o Windows Vista. Windows Programma di installazione Windows Server 2003 o Windows XP. Vedere i [Windows di installazione Run-Time](windows-installer-portal.md) per informazioni sul Service Pack minimo Windows richiesto da una versione Windows Installer.<br/> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Proprietà](properties.md)
</dt> <dt>

[**MsiSetInternalUI**](/windows/desktop/api/Msi/nf-msi-msisetinternalui)
</dt> <dt>

[**ARPNOMODIFY**](arpnomodify.md)
</dt> </dl>

 

 




