---
description: Fornisce un modello per la creazione di class factory.
ms.assetid: 3dbe6402-15f8-4490-9fe2-bebaa4e79170
title: Classe CFactoryTemplate (ComBase. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CFactoryTemplate
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: be5ca9b8319eeddf777cbf0071c1930f21524369
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106329814"
---
# <a name="cfactorytemplate-class"></a>Classe CFactoryTemplate

Fornisce un modello per la creazione di class factory.

In DirectShow, le class factory sono specializzate mediante la classe **CFactoryTemplate** , denominata anche *modello Factory*. Ogni class factory include un puntatore a un modello Factory. Il modello Factory contiene informazioni su un oggetto COM, incluso l'identificatore di classe (CLSID) dell'oggetto e un puntatore a una funzione che crea l'oggetto.

Nella DLL dichiarare una matrice globale di modelli Factory denominati *g \_ templates*. Includere un modello di Factory per ogni oggetto della DLL. Quando la funzione [**DllGetClassObject**](/windows/desktop/api/combaseapi/nf-combaseapi-dllgetclassobject) crea un nuovo class factory, Cerca nella matrice un modello con un CLSID corrispondente. Presumendo che ne trovi uno, viene creato un class factory che include un puntatore al modello corrispondente. Quando il client chiama **IClassFactory:: CreateInstance**, il class factory chiama la funzione di creazione di istanze definita nel modello.

Per ulteriori informazioni, vedere [How to create an DirectShow Filter DLL](how-to-create-a-dll.md).



| Variabili membro pubblico                                                   | Descrizione                                                                |
|---------------------------------------------------------------------------|----------------------------------------------------------------------------|
| [**\_nome m**](cfactorytemplate-m-name.md)                                | Nome del filtro.                                                        |
| [**\_CLSID m**](cfactorytemplate-m-clsid.md)                              | Puntatore al CLSID dell'oggetto.                                        |
| [**\_lpfnNew m**](cfactorytemplate-m-lpfnnew.md)                          | Puntatore a una funzione che crea un'istanza dell'oggetto.              |
| [**\_lpfnInit m**](cfactorytemplate-m-lpfninit.md)                        | Puntatore a una funzione che viene chiamata dal punto di ingresso della DLL.           |
| [**\_filtro pAMovieSetup \_ m**](cfactorytemplate-m-pamoviesetup-filter.md) | Puntatore a una struttura di [**\_ filtro AMOVIESETUP**](amoviesetup-filter.md) . |
| Metodi pubblici                                                            | Descrizione                                                                |
| [**IsClassID**](cfactorytemplate-isclassid.md)                           | Determina se un CLSID corrisponde a questo modello di classe.                    |
| [**CreateInstance**](cfactorytemplate-createinstance.md)                 | Chiama la funzione di creazione di oggetti per la classe.                          |



 

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>ComBase. h (Includi Streams. h)</dt> </dl>                                                    |
| Libreria<br/> | <dl> <dt>Strmbase. lib; </dt> <dt>Strmbasd. lib</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Riferimento alla classe di base](base-class-reference.md)
</dt> </dl>

 

