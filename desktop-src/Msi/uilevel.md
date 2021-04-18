---
description: Il programma di installazione imposta la proprietà UILevel sul livello dell'interfaccia utente.
ms.assetid: 9fc58026-f140-4218-b44f-50fc6b0ef3e9
title: Proprietà UILevel
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 83b48ebaeb246f42e552b93c974db92c78e54dbc
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106327918"
---
# <a name="uilevel-property"></a>Proprietà UILevel

Il programma di installazione imposta la proprietà **UILevel** sul livello dell'interfaccia utente. L'interfaccia utente interna è abilitata e impostata da [**MsiSetInternalUI**](/windows/desktop/api/Msi/nf-msi-msisetinternalui). Questa proprietà è impostata su uno dei tipi di dati INSTALLUILEVEL seguenti.



| INSTALLUILEVEL          | Valore numerico | Livello dell'interfaccia utente                        |
|-------------------------|---------------|---------------------------------------------|
| INSTALLUILEVEL \_ None    | 2             | Installazione invisibile all'utente.             |
| INSTALLUILEVEL \_ Basic   | 3             | Semplice gestione degli errori e dello stato di avanzamento.         |
| INSTALLUILEVEL \_ ridotto | 4             | Interfaccia utente creata, finestre di dialogo della procedura guidata eliminati.     |
| INSTALLUILEVEL \_ completo    | 5             | Interfaccia utente creata con procedure guidate, stato, errori. |



 

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Versione<br/> | Windows Installer 5,0 in Windows Server 2012, Windows 8, Windows Server 2008 R2 o Windows 7. Windows Installer 4,0 o Windows Installer 4,5 in Windows Server 2008 o Windows Vista. Windows Installer in Windows Server 2003 o Windows XP. Vedere i [requisiti di Run-Time Windows Installer](windows-installer-portal.md) per informazioni sul Service Pack minimo di Windows richiesto da una versione Windows Installer.<br/> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Proprietà](properties.md)
</dt> <dt>

[Interfaccia utente](user-interface.md)
</dt> <dt>

[Determinazione del livello dell'interfaccia utente da un'azione personalizzata](determining-ui-level-from-a-custom-action.md)
</dt> </dl>

 

 




