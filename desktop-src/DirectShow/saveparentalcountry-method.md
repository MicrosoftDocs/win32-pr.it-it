---
description: Il metodo DVDAdm. SaveParentalCountry Salva il nuovo paese/area padre dell'applicazione nel registro di sistema.
ms.assetid: 2185ad7d-c7c1-4d8b-82e7-5ed5fffaff26
title: Metodo SaveParentalCountry (Segment. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c9ca47a6ca10f25298b4eb10fdcf532c8d764b96
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106328609"
---
# <a name="saveparentalcountry-method"></a>Metodo SaveParentalCountry

> [!Note]  
> Questo componente è disponibile per l'uso nei sistemi operativi Microsoft Windows 2000, Windows XP e Windows Server 2003. È possibile che in versioni successive sia stata modificata o non sia più disponibile.

 

Il `DVDAdm.SaveParentalCountry` metodo salva il nuovo paese/area padre dell'applicazione nel registro di sistema.

``` syntax
DVD.DVDAdm.SaveParentalCountry(iCountry, sUserName, sPassword)
```

## <a name="parameters"></a>Parametri

<dl> <dt>

<span id="iCountry"></span><span id="icountry"></span><span id="ICOUNTRY"></span>*iCountry*
</dt> <dd>

Specifica il paese/area padre come intero.

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

Questo metodo consente a un utente che conosce la password corrente di salvare una nuova impostazione del paese padre/area geografica nel registro di sistema. Come per tutti i metodi di **MSDVDAdm**, questo metodo non influisce sul livello corrente del lettore. modifica solo l'impostazione del registro di sistema, in modo che la volta successiva che viene creato l'oggetto MSWebDVD verrà aperto con il nuovo paese/area geografica. Per modificare il paese padre/area geografica nel lettore, chiamare [**SelectParentalCountry**](selectparentalcountry-method.md), che non modifica l'impostazione del registro di sistema.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------|--------------------------------------------------------------------------------------|
| Intestazione<br/> | <dl> <dt>Segmento. h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**SaveParentalLevel**](saveparentallevel-method.md)
</dt> <dt>

[Oggetto MSDVDAdm](msdvdadm-object.md)
</dt> </dl>

 

 




