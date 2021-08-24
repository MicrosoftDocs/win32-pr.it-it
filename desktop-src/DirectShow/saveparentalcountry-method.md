---
description: Il metodo DVDAdm.SaveParentalCountry salva il nuovo paese/area genitori dell'applicazione nel Registro di sistema.
ms.assetid: 2185ad7d-c7c1-4d8b-82e7-5ed5fffaff26
title: Metodo SaveParentalCountry (Segment.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9d5391982129c799e6a565da362837a557765cf46604653f4f702ed38dcb910e
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119651211"
---
# <a name="saveparentalcountry-method"></a>Metodo SaveParentalCountry

> [!Note]  
> Questo componente è disponibile per l'uso nei sistemi operativi Microsoft Windows 2000, Windows XP e Windows Server 2003. È possibile che in versioni successive sia stata modificata o non sia più disponibile.

 

Il `DVDAdm.SaveParentalCountry` metodo salva il nuovo paese/area genitori dell'applicazione nel Registro di sistema.

``` syntax
DVD.DVDAdm.SaveParentalCountry(iCountry, sUserName, sPassword)
```

## <a name="parameters"></a>Parametri

<dl> <dt>

<span id="iCountry"></span><span id="icountry"></span><span id="ICOUNTRY"></span>*iCountry*
</dt> <dd>

Specifica il paese/area geografica del padre come integer.

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

Questo metodo consente a un utente che conosce la password corrente di salvare una nuova impostazione del paese/area geografica dei genitori nel Registro di sistema. Come per tutti i metodi di **MSDVDAdm,** questo metodo non influisce sul livello corrente nel lettore. modifica solo l'impostazione del Registro di sistema, in modo che alla successiva creazione dell'oggetto MSWebDVD, si aprirà con il nuovo paese/area geografica. Per modificare il paese/area geografica del lettore, chiamare [**SelectParentalCountry**](selectparentalcountry-method.md), che non modifica l'impostazione del Registro di sistema.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------|--------------------------------------------------------------------------------------|
| Intestazione<br/> | <dl> <dt>Segment.h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**SaveParentalLevel**](saveparentallevel-method.md)
</dt> <dt>

[Oggetto MSDVDAdm](msdvdadm-object.md)
</dt> </dl>

 

 




