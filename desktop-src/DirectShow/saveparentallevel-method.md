---
description: Il metodo DVDAdm. SaveParentalLevel salva un nuovo livello padre predefinito nel registro di sistema.
ms.assetid: 8ad22098-acbd-41fd-9224-829b3cc5f8ae
title: Metodo SaveParentalLevel (Segment. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 94d30d26264dff077de391b6b513f7e9ab5048c8
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106328606"
---
# <a name="saveparentallevel-method"></a>Metodo SaveParentalLevel

> [!Note]  
> Questo componente è disponibile per l'uso nei sistemi operativi Microsoft Windows 2000, Windows XP e Windows Server 2003. È possibile che in versioni successive sia stata modificata o non sia più disponibile.

 

Il metodo **DVDAdm. SaveParentalLevel** salva un nuovo livello padre predefinito nel registro di sistema.

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

Specifica il nome utente sotto forma di stringa. (Attualmente ignorata).

</dd> <dt>

<span id="sPassword"></span><span id="spassword"></span><span id="SPASSWORD"></span>*sPassword*
</dt> <dd>

Specifica la password sotto forma di stringa.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Nessun valore restituito.

## <a name="remarks"></a>Commenti

Questo metodo consente a un utente che conosce la password corrente di salvare una nuova impostazione del livello padre nel registro di sistema. Come per tutti i metodi di **MSDVDAdm**, questo metodo non influisce sul livello corrente del lettore. viene modificata solo l'impostazione del registro di sistema, in modo che la volta successiva in cui viene avviato l'oggetto MSWebDVD verrà aperto con il nuovo livello. Specificare-1 per disabilitare la gestione padre. Per modificare il livello padre nel lettore, chiamare [**SelectParentalLevel**](selectparentallevel-method.md), che non modifica l'impostazione del registro di sistema.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------|--------------------------------------------------------------------------------------|
| Intestazione<br/> | <dl> <dt>Segmento. h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Oggetto MSDVDAdm](msdvdadm-object.md)
</dt> </dl>

 

 




