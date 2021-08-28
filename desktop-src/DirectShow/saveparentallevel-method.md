---
description: Il metodo DVDAdm.SaveParentalLevel salva un nuovo livello di genitori predefinito nel Registro di sistema.
ms.assetid: 8ad22098-acbd-41fd-9224-829b3cc5f8ae
title: Metodo SaveParentalLevel (Segment.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0e372563a6f5a1fe8e893efeb86633baa6a03a7b72c79e3f05a3ec7372bec2e0
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119315951"
---
# <a name="saveparentallevel-method"></a>Metodo SaveParentalLevel

> [!Note]  
> Questo componente è disponibile per l'uso nei sistemi operativi Microsoft Windows 2000, Windows XP e Windows Server 2003. È possibile che in versioni successive sia stata modificata o non sia più disponibile.

 

Il **metodo DVDAdm.SaveParentalLevel** salva un nuovo livello di genitori predefinito nel Registro di sistema.

``` syntax
DVD.DVDAdm.SaveParentalLevel(iLevel, sUserName, sPassword)
```

## <a name="parameters"></a>Parametri

<dl> <dt>

<span id="iLevel"></span><span id="ilevel"></span><span id="ILEVEL"></span>*iLevel*
</dt> <dd>

Specifica il livello padre come valore anInteger compreso tra 1 e 8.

</dd> <dt>

<span id="sUserName"></span><span id="susername"></span><span id="SUSERNAME"></span>*sUserName*
</dt> <dd>

Specifica il nome utente come stringa. (Attualmente ignorato).

</dd> <dt>

<span id="sPassword"></span><span id="spassword"></span><span id="SPASSWORD"></span>*sPassword*
</dt> <dd>

Specifica la password come stringa.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Nessun valore restituito.

## <a name="remarks"></a>Commenti

Questo metodo consente a un utente che conosce la password corrente di salvare una nuova impostazione del livello genitori nel Registro di sistema. Come per tutti i metodi di **MSDVDAdm,** questo metodo non influisce sul livello corrente nel lettore. modifica solo l'impostazione del Registro di sistema, in modo che al successivo avvio dell'oggetto MSWebDVD, si aprirà con il nuovo livello. Specificare -1 per disabilitare la gestione dei genitori. Per modificare il livello di genitori nel lettore, chiamare [**SelectParentalLevel**](selectparentallevel-method.md), che non modifica l'impostazione del Registro di sistema.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------|--------------------------------------------------------------------------------------|
| Intestazione<br/> | <dl> <dt>Segment.h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Oggetto MSDVDAdm](msdvdadm-object.md)
</dt> </dl>

 

 




