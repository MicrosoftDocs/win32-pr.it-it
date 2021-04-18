---
description: Il programma di installazione imposta la proprietà ProductState sullo stato di installazione del prodotto in fase di inizializzazione.
ms.assetid: 833e9a15-10f8-4b1c-945f-bc02b506f627
title: Proprietà ProductState
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a51ea88058aa8bae6b67acaea96b506a7560c7a2
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106333975"
---
# <a name="productstate-property"></a>Proprietà ProductState

Il programma di installazione imposta la proprietà **ProductState** sullo stato di installazione del prodotto in fase di inizializzazione. Questa proprietà è impostata su uno dei seguenti tipi di dati INSTALLSTATE restituiti da [**MsiQueryProductState**](/windows/desktop/api/Msi/nf-msi-msiqueryproductstatea).



| INSTALLSTATE             | Valore numerico | Stato di installazione del prodotto                   |
|--------------------------|---------------|-------------------------------------------------|
| INSTALLSTATE \_ sconosciuto    | -1            | Il prodotto non è né annunciato né installato. |
| INSTALLSTATE \_ annunciata | 1             | Il prodotto è annunciato ma non è installato.    |
| INSTALLSTATE \_ assente     | 2             | Il prodotto viene installato per un utente diverso.  |
| \_impostazione predefinita InstallState    | 5             | Il prodotto è installato per l'utente corrente.  |



 

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Versione<br/> | Windows Installer 5,0 in Windows Server 2012, Windows 8, Windows Server 2008 R2 o Windows 7. Windows Installer 4,0 o Windows Installer 4,5 in Windows Server 2008 o Windows Vista. Windows Installer in Windows Server 2003 o Windows XP. Vedere i [requisiti di Run-Time Windows Installer](windows-installer-portal.md) per informazioni sul Service Pack minimo di Windows richiesto da una versione Windows Installer.<br/> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Proprietà](properties.md)
</dt> </dl>

 

 




